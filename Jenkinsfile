pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git credentialsId: '0d89a143-e44e-4f0e-9968-65978a0bc0b2', url: 'https://github.com/nukalavarshita/todo-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t python-todo-cli .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run --rm python-todo-cli'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
