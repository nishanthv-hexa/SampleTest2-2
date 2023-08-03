pipeline {
    agent any

     stages {
        stage('Build') {
            steps {
                git 'https://github.com/nishanthv-hexa/SampleTest2-2.git'
            }
            }
     }
        stage('Dependency Track'){
            steps{
                dependencyTrackPublisher artifact: 'broken1.json', autoCreateProjects: false, dependencyTrackApiKey: '', dependencyTrackFrontendUrl: '', dependencyTrackUrl: '', projectId: '3f28f483-d207-491d-b784-6ee5ee157ccc', synchronous: true
            }
        }

}
 
