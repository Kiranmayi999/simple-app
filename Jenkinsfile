pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/kiranmayi999/simple-app.git'
            }
        }
        stage('Build') {
            steps {
                echo 'No build needed for this simple app'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying Simple App...'
                // Add deploy commands here if you want
            }
        }
    }
}
