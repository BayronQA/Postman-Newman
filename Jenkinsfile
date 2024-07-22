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
                    // Asumiendo que Newman está en el PATH, simplemente usa 'newman'
                    bat 'newman run C:\\Users\\Bayron\\Desktop\\Postman-POC-Previred\\POC-Previred_Postman.postman_collection.json -e C:\\Users\\Bayron\\Desktop\\Postman-POC-Previred\\Ambiente_POC-Previred.postman_environment.json'
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
