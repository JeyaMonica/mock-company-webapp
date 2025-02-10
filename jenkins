pipeline {
    agent {
        docker {
            image 'node:18' // Use official Node.js 18 Docker image
        }
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm  // Fetch repository code
            }
        }

        stage('Verify Node.js') {
            steps {
                script {
                    sh 'node -v'  // Check if Node.js 18 is used
                    sh 'npm -v'   // Check npm version
                }
            }
        }

        stage('Build') {
            steps {
                script {
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
