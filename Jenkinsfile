pipeline {
    agent any
    tools {
        nodejs 'NodeJS'  // Nombre de la instalación de NodeJS configurada en Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Clonar el repositorio de GitHub usando el token de acceso personal
                    withCredentials([string(credentialsId: 'github-token', variable: 'GITHUB_TOKEN')]) {
                        sh 'git clone https://$GITHUB_TOKEN@github.com/BayronQA/Postman-Newman.git'
                        dir('Postman-Newman') {
                            sh 'git checkout main'
                        }
                    }
                }
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
                    bat 'newman run Postman-Newman/POC-Previred_Postman.postman_collection.json -e Postman-Newman/Ambiente_POC-Previred.postman_environment.json'
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
