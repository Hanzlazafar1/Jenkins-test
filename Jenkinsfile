pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // This step checks out the code from your GitHub repository
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building...'
                // For a simple Python script, there isn't much to "build".
                // If you had dependencies, you would install them here (e.g., pip install -r requirements.txt)
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running unit tests...'
                // Note: Using 'bat' for Windows Jenkins server. If your Jenkins is on Linux, change 'bat' to 'sh'.
                bat 'python test_app.py'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'python app.py'
            }
        }
    }
}
