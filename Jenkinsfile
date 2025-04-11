pipeline {
  agent any
  
  stages {
    stage('Install Chrome with Ansible') {
      steps {
        echo 'Running Ansible playbook to install Chrome...'
        sh '''
          ansible-playbook -i inventory install_chrome.yml
        '''
      }
    }
  }
}

