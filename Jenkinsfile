pipeline {
    agent any

    stages {
        stage('Clonar repositório') {
            steps {
                git branch: 'main', url: 'https://github.com/gidias1/Modulo-13.git'
            }
        }

        stage('Instalar dependências') {
            steps {
                bat 'npm install'
            }
        }

        stage('Executar testes de API') {
            steps {
                bat 'npx mocha test/**/*.js'
            }
        }
    }
}
