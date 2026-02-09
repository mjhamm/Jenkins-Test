pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Jenkins pulls the code from GitHub automatically here
                checkout scm
            }
        }
        stage('Debug and Run') {
            steps {
                // List files to make sure script.py is there
                bat 'dir' 
                // Print python version to make sure it's installed
                bat 'python --version'
                // Run unbuffered
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
