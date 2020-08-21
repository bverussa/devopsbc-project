pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo "Updating git submodule"
        sh 'git submodule update --recursive --remote'
      }
    }    
    stage('Deploy') {
      steps {
        echo "Executing Ansible Playbook"
        sh 'ssh bruno@10.211.55.4 "cd /home/bruno/workspace/devopsbc-project && ansible-playbook playbook_deploy.yml"'
      }
    }
  }
}
