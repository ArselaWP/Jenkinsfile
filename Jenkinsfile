pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t mustikaningrum/flask-hello-world:%BUILD_NUMBER% .'
            }
        }

        stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub-credentials',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {
                    bat 'echo|set /p="%DOCKER_PASS%" | docker login -u %DOCKER_USER% --password-stdin'
                    bat 'docker push mustikaningrum/flask-hello-world:%BUILD_NUMBER%'
                }
            }
        }
    }
}
