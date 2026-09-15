pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checked out from GitHub'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                echo 'Test passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment completed!'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
