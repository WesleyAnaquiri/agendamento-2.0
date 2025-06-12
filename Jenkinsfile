pipeline {
    agent any

    stages {
        stage('Clonar projeto') {
            steps {
                git 'https://github.com/WesleyAnaquiri/agendamento-2.0.git'

            }
        }
        stage('Build Docker') {
            steps {
                script {
                    docker.build('agendamento-app')
                }
            }
        }
        stage('Executar Container') {
            steps {
                script {
                    docker.image('agendamento-app').run()
                }
            }
        }
    }
}
