pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'  // TODO: Build the application
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'  // TODO: Run the tests
            }
        }
    }
}
