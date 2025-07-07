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
                dir('test-api/api-tests') {
                    bat 'npm install'
                }
            }
        }

        stage('Executar testes de API') {
            steps {
                dir('test-api/api-tests') {
                    bat 'npx mocha test/**/*.js'
                }
            }
        }
    }
}
