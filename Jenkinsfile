pipeline {
    agent any

     stages {
        stage('Build') {
            steps {
                git 'https://github.com/nishanthv-hexa/SampleTest2.git'
            }
            }
        stage('Dependency Track'){
            steps{
                dependencyTrackPublisher artifact: '@broken1.json', autoCreateProjects: false, dependencyTrackApiKey: '', dependencyTrackFrontendUrl: '', dependencyTrackUrl: '', projectId: '0b884a2d-66c6-4062-b1e0-5443b59c0b05', synchronous: false
            }
        }

}
 
