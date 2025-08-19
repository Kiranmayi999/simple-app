pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from your Git repository
                checkout scm
            }
        }

        stage('Validate HTML') {
            steps {
                // Example: Validate HTML using a tool, or you can skip if not needed
                echo 'Validating HTML (optional step)'
                // sh 'html-validator index.html' // Uncomment if you have validator CLI installed
            }
        }

        stage('Archive') {
            steps {
                // Archive the HTML file as a build artifact
                archiveArtifacts artifacts: 'index.html', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                // Example: copy the HTML to a web server (customize as needed)
                // For demo, just echo deployment
                echo 'Deploying to web server (implement your deployment here)'
                
                // Example scp command to remote server
                // sh 'scp index.html user@yourserver:/var/www/html/'
            }
        }
    }

    post {
        success {
            echo 'Build and deployment successful!'
        }
        failure {
            echo 'Build or deployment failed.'
        }
    }
}
