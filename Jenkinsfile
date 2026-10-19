
pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t arselawp/flask-hello-world .'
            }
        }
    }
}
