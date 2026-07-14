pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Getting code from Git'
            }
        }

        stage('Install') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build') {
            steps {
                echo 'Application built successfully'
            }
        }
    }
}