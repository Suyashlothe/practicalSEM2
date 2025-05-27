pipeline {
    agent any

    environment {
        // Optional: set up any environment variables
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Running build..."
                // Example build command
                sh './build.sh'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                // Example test command
                sh './run-tests.sh'
            }
        }
    }

    post {
        always {
            echo "Job completed."
        }
        success {
            echo "Build succeeded!"
        }
        failure {
            echo "Build failed."
        }
    }
}
