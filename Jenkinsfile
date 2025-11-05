pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building application..."
                bat '"C:\\Users\\HP\\AppData\\Local\\Microsoft\\WindowsApps\\PythonSoftwareFoundation.Python.3.11_qbz5n2kfra8p0\\python.exe" --version'

            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                bat "\"C:\\Users\\HP\\AppData\\Local\\Microsoft\\WindowsApps\\PythonSoftwareFoundation.Python.3.11_qbz5n2kfra8p0\\python.exe\" -m pip install --upgrade pip"
                bat "\"C:\\Users\\HP\\AppData\\Local\\Microsoft\\WindowsApps\\PythonSoftwareFoundation.Python.3.11_qbz5n2kfra8p0\\python.exe\" -m pip install pytest"
                bat "\"C:\\Users\\HP\\AppData\\Local\\Microsoft\\WindowsApps\\PythonSoftwareFoundation.Python.3.11_qbz5n2kfra8p0\\python.exe\" -m pytest -q"

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
