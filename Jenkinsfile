pipeline {
    agent { docker { image 'python:3.7' } }
    stages {
        stage('build') {
            steps {
                withEnv(["HOME=${env.WORKSPACE}"]) {
                    sh "pip3 install pytest --user"
                    sh ' python3 -m pytest pytest/test_add.py'
                }
            }
        }
    }
}
