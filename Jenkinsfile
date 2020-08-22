pipeline {
  agent any
  environment {
      GIT_SSH_COMMAND = 'ssh -i ~/.ssh/id_rsa'
  }
  stages {   
    stage('Deploy') {
      steps {
        echo "Executing Ansible Playbook"
        sh 'ssh bruno@10.211.55.4 "cd /home/bruno/workspace/devopsbc-project && ansible-playbook playbook_deploy.yml"'
      }
    }
  }
}
