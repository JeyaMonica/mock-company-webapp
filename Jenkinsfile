pipeline {
    agent any

    tools {
        maven 'Maven 3.9.9'  // Ensure this matches the Maven version in Jenkins
          // Ensure Java 8 is configured in Jenkins
    }

    environment {
        MAVEN_OPTS = "-Dmaven.repo.local=.m2/repository"
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    echo 'Checking out source code...'
                }
                checkout scm
            }
        }

        stage('Build') {
            steps {
                script {
                    echo 'Building the application...'
                }
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                }
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying application...'
                }
                // Add deployment steps here if needed
            }
        }
    } // Ensure this closing brace is present

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
    }
} // This closing brace was likely missing
