pipeline {
    agent any

    tools {
        // Use appropriate tools if required
        // e.g., jdk 'jdk11', maven 'maven3'
    }

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning the repository...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building...'
                // Example build command
                sh './build.sh'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                // Example test command
                sh './run-tests.sh'
            }
        }
    }

    post {
        success {
            echo 'Build and tests succeeded.'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
