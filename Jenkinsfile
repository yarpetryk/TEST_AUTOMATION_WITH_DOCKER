pipeline {
    agent any
    stages {
        stage('Run automated test') {
            steps {
                echo 'Running pipeline...'
                sh 'docker compose -f docker-compose.yml up -d --build'
            }
        }
    }
}