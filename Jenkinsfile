
pipeline {
    agent any

    environment {
       bat 'docker build -t arselawp/hello-world-docker .'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t %IMAGE_NAME% .'
            }
        }
    }
}
