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
<<<<<<< HEAD
                sh 'docker build -t gaming-app .'
=======
                echo 'Gaming App Version 2'
>>>>>>> c5e60234f1ebdedaf3b52147006ebdcfbc4e6248
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

    post {
        success {
            echo 'Application deployed successfully'
        }
    }
}
