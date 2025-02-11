pipeline {
    agent any  // Runs on any available Jenkins agent

    stages {
        stage('Checkout') {
            steps {
                // Cloning the repository
                git 'https://github.com/JeyaMonica/mock-company-webapp.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'mvn clean install'  // Run Maven build
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'  // Run unit tests
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Deployment steps (if needed)
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully! 🎉'
        }
        failure {
            echo 'Pipeline failed! ❌'
        }
    }
}
