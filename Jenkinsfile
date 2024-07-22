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
                    // Usar la ruta completa de newman.cmd o newman.exe
                    bat 'C:\\Users\\Bayron\\AppData\\Roaming\\npm\\newman.cmd run C:\\Users\\Bayron\\Desktop\\Postman-POC-Previred\\POC-Previred_Postman.postman_collection.json -e C:\\Users\\Bayron\\Desktop\\Postman-POC-Previred\\Ambiente_POC-Previred.postman_environment.json'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
