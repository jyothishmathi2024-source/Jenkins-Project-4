pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/jyothishmathi2024-source/Jenkins-Project-4.git'
            }
        }

        stage('Show Build Info') {
            steps {
                echo "Build Number: ${env.BUILD_NUMBER}"
                echo "Job Name: ${env.JOB_NAME}"
                echo "Workspace: ${env.WORKSPACE}"
            }
        }

        stage('Run Linter') {
            steps {
                bat 'python -m flake8 app.py'
            }
        }
    }
}