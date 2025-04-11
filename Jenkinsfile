pipeline {
    agent any

    stages {
        stage('Debug Info') {
            steps {
                echo "===== WHOAMI ====="
                sh 'whoami'

                echo "===== ENV ====="
                sh 'printenv'

                echo "===== WHERE IS ANSIBLE ====="
                sh 'which ansible-playbook'

                echo "===== ANSIBLE VERSION ====="
                sh 'ansible-playbook --version'
            }
        }

        stage('Run Playbook') {
            steps {
                echo "===== RUNNING ANSIBLE PLAYBOOK ====="
                sh 'ansible-playbook playbook.yml'
            }
        }
    }
}

