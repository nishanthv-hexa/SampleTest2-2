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

        stage('Snyk'){
            steps{
                snykSecurity failOnIssues: false, organisation: 'hex', projectName: 'Sample', snykInstallation: 'Snyk1', snykTokenId: 'd18895ab-63cf-472e-b2c9-738958f7baf6', targetFile: '/var/lib/jenkins/workspace/Sampletest2/'
            }
        }
     }
}
 
