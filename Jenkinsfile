pipeline {
    agent any

    stages {

        stage('Check Python') {
            steps {
                sh 'python3 --version'
                sh 'python3 -m pip --version'
            }
        }

        stage('Upgrade Pip') {
            steps {
                sh 'python3 -m pip install --upgrade pip'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'python3 -m pytest'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Successful!'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }

        failure {
            echo 'Pipeline failed. Check the Console Output for details.'
        }

        always {
            echo 'Pipeline execution finished.'
        }
    }
}