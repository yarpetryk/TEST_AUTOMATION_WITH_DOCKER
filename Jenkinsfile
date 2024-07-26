pipeline {
    agent any
    stages {
        stage('Before running') {
            steps {
                echo 'Prepare for test running'
            }
        }
        stage('Run automated test') {
            steps {
                echo 'Running pipeline...'
                sh 'docker compose -f docker-compose.yml up -d --build'
            }
        }
    }
    post {
        always {
            mail to: 'yaroslav.petryk@lembergsolutions.com',
                 subject: "Pipeline is running",
                 body: "Pipeline is running"
            echo 'Pipeline is running'
        }
        success {
            mail to: 'yaroslav.petryk@lembergsolutions.com',
                 subject: "Pipeline finished with success",
                 body: "SUCCESS!!!"
        }
        failure {
            mail to: 'yaroslav.petryk@lembergsolutions.com',
                 subject: "Pipeline finished with failure",
                 body: "ERROR!!!"
        }
    }
}