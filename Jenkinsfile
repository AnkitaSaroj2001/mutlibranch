pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from your version control system (e.g., Git)
                git 'https://github.com/AnkitaSaroj2001/mutlibranch.git'
                
            }
        }
        
        stage('Build') {
            steps {
                // Build your Maven project
                sh 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                // Run your tests
                sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy your application (this is just an example, adjust it according to your deployment process)
                sh 'mvn deploy'
            }
        }
    }
    
    post {
        success {
            // Notification or further actions if the pipeline succeeds
            echo 'Pipeline succeeded!'
        }
        failure {
            // Notification or further actions if the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
