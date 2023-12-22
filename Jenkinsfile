pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the source code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'npm install'  // replace with your actual build command
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test'  // replace with your actual test command
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment commands here (e.g., copy files to a server)
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Notify stakeholders or perform additional actions.'
        }
        failure {
            echo 'Pipeline failed! Notify the team or take corrective actions.'
        }
    }
}
