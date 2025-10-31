pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building application..."
                sh 'python --version'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh "pip install pytest"
                sh "pytest -q"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                sh 'echo "App deployed successfully!"'
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully."
        }
        failure {
            echo "Pipeline failed."
        }
    }
}
