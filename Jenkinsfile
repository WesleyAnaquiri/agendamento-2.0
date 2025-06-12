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
