pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building website...'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing website...'
                sh 'test -f index.html'
                echo 'Website test passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying website to Apache...'
                sh 'sudo cp index.html /var/www/html/index.html'
                echo 'Website deployed successfully!'
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
