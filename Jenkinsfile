pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t gaming-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker rm -f gaming-app || true
                docker run -d --name gaming-app -p 80:80 gaming-app
                '''
            }
        }
    }
}
