pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'No build step for now'
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
                // Add real deploy command here if needed
            }
        }
    }
}
