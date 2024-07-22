pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                script {
                    bat 'node C:\\Users\\Bayron\\AppData\\Roaming\\npm\\newman run C:\\Users\\Bayron\\Desktop\\Postman-POC-Previred\\POC-Previred_Postman.postman_collection.json -e C:\\Users\\Bayron\\Desktop\\Postman-POC-Previred\\Ambiente_POC-Previred.postman_environment.json'
                }
