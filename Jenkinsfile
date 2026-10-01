pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Validate') {
            steps {
                sh 'echo "Validating Ansible project..."'
                sh 'ls -la'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploy stage - Ansible will run here"'
            }
        }

    }
}
