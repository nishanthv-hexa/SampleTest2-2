pipeline {
    agent any

     stages {
        stage('Build') {
            steps {
                git 'https://github.com/nishanthv-hexa/SampleTest2-2.git'
            }
            }
     
        // stage('Dependency Track'){
        //     steps{
        //         dependencyTrackPublisher artifact: 'broken1.json', autoCreateProjects: true, dependencyTrackApiKey: '', dependencyTrackFrontendUrl: '', dependencyTrackUrl: '', projectId: '3e1e5c6b-1c66-4a20-94c6-0c8267a7ef8e', synchronous: true
        //     }
        // }
        //stage('Linting') {
        //     steps {
        //         script {
        //             // Navigate to your project's directory
        //             dir('/home/hexa/vulnerable-node') {
        //                 // Run ESLint against your source code
        //                 sh 'npx eslint src'
        //             }
        //         }
        //     }
        // }
        stage('Snyk'){
            steps{
                snykSecurity failOnIssues: false, organisation: '94d1ccfd-eac2-4e0c-82ac-6d39b06b2bd1', projectName: 'Sample', snykInstallation: 'Snyk1', snykTokenId: 'Api2', targetFile: '/var/lib/jenkins/workspace/Sampletest2/package-lock.json'
            }
        }
        stage('Clair'){
            steps{
                sh "clair-scanner -c http://localhost:6060 --ip 172.17.0.1 --report=’nodelates.json’ node:latest"
            }
        }
        stage('Sslyze'){
            steps{
                sh "sslyze test.atop-da.com --json_out sslyze.json || true"
            }
        }
     }
}
 
