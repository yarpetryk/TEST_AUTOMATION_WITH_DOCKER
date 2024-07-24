pipeline {
    agent any
    stages {
        stage('Run automated test') {
            steps {
                sh 'docker stop $(docker ps -a -q)'
                sh 'docker rm $(docker ps -a -q)'
                sh 'docker compose -f docker-compose.yml up -d --build'
            }
        }
    }
}