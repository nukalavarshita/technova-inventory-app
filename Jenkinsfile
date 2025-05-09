# Use the official Node.js image
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the application port (default for Node.js is 3000)
EXPOSE 3000

# Command to run the app
CMD ["npm", "start"]
# Use the official Node.js image
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the application port (default for Node.js is 3000)
EXPOSE 3000

# Command to run the app
CMD ["npm", "start"]
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
}pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/nukalavarshita/technova-inventory-app.git'
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

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
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
  }# Use the official Node.js image
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose the application port (default for Node.js is 3000)
EXPOSE 3000

# Command to run the app
CMD ["npm", "start"]
}
