pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'  // TODO: Ensure this works
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'  // TODO: Ensure this works
            }
        }
    }
}

