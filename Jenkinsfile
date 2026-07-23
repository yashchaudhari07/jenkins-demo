pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-html-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8081:80 --name html-container my-html-app'
            }
        }
        stage('Push Image') {
            steps {
               bat 'docker push yashchaudhari07/my-html-app'
            }
        }
    }
}