pipeline {
    agent {
        docker {
            image 'node:18' // Use Node.js 18 Docker image
        }
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'node -v'  // Verify Node.js version
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
