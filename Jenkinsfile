pipeline {
    agent any

     stages {
        stage('Build') {
            steps {
                git 'https://github.com/nishanthv-hexa/SampleTest2-2.git'
            }
            }
     
        stage('Dependency Track'){
            steps{
                dependencyTrackPublisher artifact: 'broken1.json', autoCreateProjects: false, dependencyTrackApiKey: '', dependencyTrackFrontendUrl: '', dependencyTrackUrl: '', projectId: '3f28f483-d207-491d-b784-6ee5ee157ccc', synchronous: true
            }
        }

        stage('Snyk'){
            steps{
                snykSecurity failOnIssues: false, organisation: 'hex', projectName: 'Sample', snykInstallation: 'Please define a Snyk installation in the Jenkins Global Tool Configuration. This task will not run without a Snyk installation.', snykTokenId: 'd18895ab-63cf-472e-b2c9-738958f7baf6', targetFile: '/var/lib/jenkins/Sampletest2/'
            }
        }
     }
}
 
