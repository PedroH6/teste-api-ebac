pipeline {
    agent any

    stages {
        stage('Clonar o repositório') {
            steps {
               git branch: 'main', url: 'https://github.com/PedroH6/teste-api-ebac.git'
            }
        }
        stage('instalar dependências') {
            steps {
                sh 'npm install'
            }
        }
        stage('executar testes') {
            steps {
                sh 'NO_COLOR=1 npm run cy:run'
            }
        }
    }
}