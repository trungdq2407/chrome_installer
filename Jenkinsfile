pipeline {
  agent any

  stages {
    stage('Debug Info') {
      steps {
        sh '''
          echo "===== WHOAMI ====="
          whoami
          
          echo "===== ENV ====="
          printenv
          
          echo "===== WHERE IS ANSIBLE ====="
          which ansible-playbook

          echo "===== RUN ANSIBLE ====="
          ansible-playbook -i inventory install_chrome.yml -vvv
        '''
      }
    }
  }
}

