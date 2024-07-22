pipeline {
    agent any
    tools {
        nodejs 'NodeJS'  // Nombre de la instalación de NodeJS configurada en Jenkins
    }
    stages {
        stage('Setup') {
            steps {
                script {
                    // Instalar Newman globalmente
                    bat 'npm install -g newman'
                }
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                script {
                    // Ejecutar Newman usando el comando instalado globalmente
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
