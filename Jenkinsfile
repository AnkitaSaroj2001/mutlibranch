pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your code repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build your application
                sh 'echo "Hello, World!" > index.html'
            }
        }

        stage('Test') {
            steps {
                // Test the application
                sh 'cat index.html'
            }
        }
    }

    post {
        always {
            // Cleanup
            sh 'rm index.html'
        }
    }
}
