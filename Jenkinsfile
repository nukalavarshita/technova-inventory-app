pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/nukalavarshita/technova-inventory-app.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t technova-inventory .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
