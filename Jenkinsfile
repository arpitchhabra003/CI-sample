pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building application..."
                bat 'python3  --version'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                bat "python3 -m pip install --upgrade pip"
                bat "pip install pytest"
                bat "pytest -q"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application..."
                bat 'echo App deployed successfully!'
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
