pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './mvnw package'
      }
    }

    stage('Ansible') {
      steps {
        sh 'ansible-playbook /home/vagrant/task.yaml --key-file /home/vagrant/.ssh/id_rsa'
      }
    }

  }
}