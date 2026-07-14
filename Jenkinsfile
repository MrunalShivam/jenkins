pipeline {
    agent any

    stages {
        stage('Check Python') {
            steps {
                sh 'python3 --version'
                sh 'python3 -m pip --version'
            }
        }

        stage('Install') {
            steps {
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'python3 -m pytest'
            }
        }
    }
}