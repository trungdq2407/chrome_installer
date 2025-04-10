pipeline {
  agent any
  
  stage {
    stage('Install chrome with Ansible') {
      step {
        echo 'Running Ansible playbook to install chrome...'
        sh'''
          ansible-playbook -i inventory install_chrome.yml
          '''
        }
      }
    }
  }
