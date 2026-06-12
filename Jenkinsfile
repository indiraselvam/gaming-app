pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code Checkout'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Gaming Application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Test Cases'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application'
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful'
        }
        failure {
            echo 'Deployment Failed'
        }
    }
}
