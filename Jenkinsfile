pipeline {
    agent any
    tools {
        nodejs 'NodeJS'  // Nombre de la instalación de NodeJS configurada en Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                // Clonar el repositorio de GitHub
                git url: 'https://github.com/BayronQA/Postman-Newman.git', branch: 'main'
            }
        }
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
                    bat 'newman run Postman-POC-Previred/POC-Previred_Postman.postman_collection.json -e Postman-POC-Previred/Ambiente_POC-Previred.postman_environment.json'
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
