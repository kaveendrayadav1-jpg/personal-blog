pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo "Pulling code from GitHub..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Running build step..."
                sh '''
                echo "Build started..."
                # Add your project build commands here
                # Example for Node app:
                # npm install

                # Example for Java Maven:
                # mvn clean package
                echo "Build completed!"
                '''
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh '''
                # Add your test commands here
                # Example:
                # npm test
                echo "Tests finished!"
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                sh '''
                # Add your deploy commands here
                # Example: copy files to a web folder
                # cp -r * /var/www/html/

                echo "Deployment completed!"
                '''
            }
        }
    }

    post {
        success {
            echo "Pipeline SUCCESS!"
        }
        failure {
            echo "Pipeline FAILED!"
        }
    }
}
