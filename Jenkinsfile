
pipeline {
    agent any

    environment {
        IMAGE_NAME = 'GANTI_DENGAN_USERNAME_DOCKERHUB/hello-world-docker'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t %IMAGE_NAME% .'
            }
        }
    }
}
