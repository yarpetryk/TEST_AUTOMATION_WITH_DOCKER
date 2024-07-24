pipeline {
    agent any
    stages {
        stage('Run automated test') {
            steps {
                sh 'docker rm /WebApp'
                sh 'docker compose -f docker-compose.yml up -d --build'
            }
        }
    }
}