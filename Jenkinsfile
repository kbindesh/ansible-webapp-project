pipeline {
  agent any
  stages {
    stage("SCM Checkout")  {
      steps {
        git "https://github.com/kbindesh/ansible-webapp-project.git"
      }
    }
    stage("Execute Ansible Playbooks") {
      steps {
        ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'inventory.ini', playbook: 'webserver-playbook.yml'
      }
    } 
  }
}