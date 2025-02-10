pipeline {
    agent any

    stages {
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
