pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Arvinth29/aws-devops-demo.git'
            }
        }

        stage('Run Python Calculator') {
            steps {
                bat 'python calculator.py'
            }
        }
    }
}