pipeline {
    agent any

    environment {
        NODE_VERSION = "18" // Specify the Node.js version
    }

    stages {
        stage('Setup Node.js') {
            steps {
                script {
                    sh 'nvm use $NODE_VERSION || nvm install $NODE_VERSION'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'node -v'  // Check if Node.js 18 is used
                    sh './gradlew assemble'  // Build the application
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './gradlew test'  // Run tests
                }
            }
        }
    }
}
