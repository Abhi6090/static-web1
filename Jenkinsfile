pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the website...'
                // For a static HTML website, this might involve linting or other tools
                sh 'echo "Build stage complete!"'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the website...'
                // Check if the HTML file exists
                sh '''
                if [ -f index.html ]; then
                    echo "Index.html exists - Test Passed!";
                else
                    echo "Index.html does not exist - Test Failed!" && exit 1;
                fi
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the website...'
                // Copy HTML files to the web server document root
                sh 'sudo cp -r * /var/www/html/'
                sh 'sudo systemctl restart apache2'
            }
        }
    }
}
