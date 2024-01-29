pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the repository
                git 'https://github.com/montabellakhal2027/Test.git'
            }
        }

        stage('Build') {
            steps {
                // Build the Java project using Maven
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests (adjust the command based on your testing framework)
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (adjust the command based on your deployment process)
                sh 'mvn deploy'
            }
        }
    }

    post {
        success {
            // Actions to perform after a successful build and deployment
            echo 'Build and deployment successful!'
        }
        failure {
            // Actions to perform if the build or deployment fails
            echo 'Build or deployment failed!'
        }
    }
}

 
