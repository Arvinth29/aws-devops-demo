pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'python3 calculator.py'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest test_calculator.py'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                mkdir -p /home/ubuntu/deploy
                cp calculator.py /home/ubuntu/deploy/
                echo "Deployment completed."
                '''
            }
        }
    }
}