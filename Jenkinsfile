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
                sh '''
                    docker run --rm \
                      -v jenkins_jenkins_home:/jenkins_home \
                      -v /var/run/docker.sock:/var/run/docker.sock \
                      -w /jenkins_home/workspace/ansible-nginx \
                      ansible-runner:latest \
                      ansible-playbook playbook.yml
                '''
            }
        }

    }
}  
