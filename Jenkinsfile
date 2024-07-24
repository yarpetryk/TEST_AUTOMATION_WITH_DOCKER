pipeline {
    agent any
    stages {
        stage('Verify docker compose') {
            steps {
                sh 'pwd'
                sh 'docker version'
            }
        }
        stage('Run automated test') {
            steps {
                sh 'docker compose -f docker-compose.yml up -d'
            }
        }
    }
}