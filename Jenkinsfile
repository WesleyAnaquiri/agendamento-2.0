pipeline {
    agent any

    stages {
        stage('Clonar projeto') {
            steps {
                git 'https://github.com/SEU_USUARIO/meu-projeto.git'
            }
        }
        stage('Build Docker') {
            steps {
                sh 'docker build -t agendamento-app .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run agendamento-app'
            }
        }
    }
}
