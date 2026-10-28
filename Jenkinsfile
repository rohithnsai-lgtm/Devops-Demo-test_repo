pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')   // Poll every 2 minutes
    }

    stages {
        stage('Checkout') {
            steps {
                echo '========== Checkout Stage =========='
                echo 'Checking out source code from Git...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo '========== Build Stage =========='
                echo 'Building the application...'
            }
        }

        stage('Test') {
            steps {
                echo '========== Test Stage =========='
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo '========== Deploy Stage =========='
                echo 'Deploying the application...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
