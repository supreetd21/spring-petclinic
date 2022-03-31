pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './mvnw package'
      }
    }

    stage('Static Analysis') {
      steps {
        withSonarQubeEnv(installationName: 'SonarQube', credentialsId: 'Sonar-Integration')
      }
    }

  }
}