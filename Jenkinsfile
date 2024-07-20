pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://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@github.com/BayronQA/Postman-Newman.git'
            }
        }
        stage('Run Postman Tests') {
            steps {
                sh 'npm install -g newman'
                sh 'newman run POC-Previred_Postman.postman_collection.json -e Ambiente_POC-Previred.postman_environment.json'
            }
        }
    }
}
