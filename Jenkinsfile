pipeline {
    agent any

    environment {
        PATH = "/var/lib/jenkins/.local/bin:${env.PATH}"
    }

    stages {
        stage('Debug Info') {
            steps {
                sh 'echo "===== WHOAMI =====" && whoami'
                sh 'echo "===== ENV =====" && printenv'
                sh 'echo "===== WHERE IS ANSIBLE =====" && which ansible-playbook'
            }
        }

        stage('Run Playbook') {
            steps {
                sh 'ansible-playbook install_chrome.yml'
            }
        }
    }
}

