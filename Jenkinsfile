pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Jenkins pulls the code from GitHub automatically here
                checkout scm
            }
        }
        stage('Execute Python') {
            steps {
                echo 'Attempting to run the python script...'
                // Use 'python' or 'python3' depending on your local installation
                bat 'python -u test.py'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
