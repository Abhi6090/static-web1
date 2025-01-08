pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // You can add build steps here if necessary
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // You can add test steps here if necessary
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Copy the HTML files to the web server directory
                sh 'cp index.html /var/www/html/'
            }
        }
    }
}
