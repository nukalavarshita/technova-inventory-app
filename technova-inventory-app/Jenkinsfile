pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/nukalavarshita/technova-inventory-app.git'
      }
    }
    stage('Test') {
      steps {
        sh 'echo "No tests defined yet."'
      }
    }
    stage('Build Docker Image') {
      steps {
        sh 'docker build -t technova-inventory .'
      }
    }
  }
}
