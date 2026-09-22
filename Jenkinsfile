pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
node {
  stage('Checkout') {
    // Checkout code from version control
    checkout scm
  }
  stage('Build') {
    // Build the application
    sh 'make all'
  }
  stage('Test') {
    // Run tests
    sh 'make test'
  }
}
