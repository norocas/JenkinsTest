pipeline {
    agent { docker { image 'python:3.7' } }
    stages {
        stage('build') {
            steps {
                withEnv(["HOME=${env.WORKSPACE}"]) {
                sh "pip install pytest --user"
                sh 'pytest pytest/'
            }
        }
    }
}
