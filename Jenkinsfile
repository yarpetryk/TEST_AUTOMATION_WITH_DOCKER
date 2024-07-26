pipeline {
    agent any
    stages {
        stage('Run automated test') {
            steps {
                echo 'Running pipeline...'
                sh 'pw'
                sh 'docker compose -f docker-compose.yml up -d --build'
            }
        }
    }
    post {
        always {
            echo 'Pipeline run is triggered'
        }
        success {
            echo 'Pipeline runs with SUCCESS'
        }
        failure {
            echo 'Pipeline runs with FAILURE'
//             mail to: 'yaroslav.petryk@lembergsolutions.com',
//                  subject: "Pipeline finished with failure",
//                  body: "ERROR!!!"
        }
    }
}