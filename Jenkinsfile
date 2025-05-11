pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'technova-inventory'
        DOCKER_TAG = 'latest'
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/nukalavarshita/technova-inventory-app.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Installing dependencies and building the application...'
                // Replace below with actual build commands
                sh 'npm install || true'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Replace below with real test commands
                sh 'npm test || echo "No tests found or tests failed (placeholder)."'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh "docker build -t ${DOCKER_IMAGE}:${DOCKER_TAG} ."
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application container...'
                // Stop any existing container with same name
                sh "docker rm -f ${DOCKER_IMAGE} || true"
                // Run new container
                sh "docker run -d --name ${DOCKER_IMAGE} -p 3000:3000 ${DOCKER_IMAGE}:${DOCKER_TAG}"
            }
        }
    }
}
