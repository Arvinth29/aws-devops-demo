pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Arvinth29/aws-devops-demo.git'
            }
        }

        stage('Check Python') {
            steps {
                sh 'python3 --version || python --version'
            }
        }
    }
}