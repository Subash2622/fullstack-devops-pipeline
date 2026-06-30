pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Verify Docker') {
            steps {
                sh 'docker --version'
                sh 'docker compose version'
            }
        }

        stage('Go to Project') {
            steps {
                sh 'cd /workspace && pwd && ls -la'
            }
        }

        stage('Build and Deploy') {
            steps {
                sh '''
                    cd /workspace
                    docker compose down
                    docker compose up -d --build
                '''
            }
        }

    }

    post {
        success {
            echo 'Application deployed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}