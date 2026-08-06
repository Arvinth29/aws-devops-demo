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
                      mkdir -p deploy
                      cp calculator.py deploy/
                      echo "Deployment completed."
                      ls -l deploy
        '''
    }
        }
    }
}