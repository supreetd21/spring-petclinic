pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh './mvnw package'
      }
    }

    stage('') {
      steps {
        sh '''mvn sonar:sonar \\
  -Dsonar.projectKey=JenkinsIntegration \\
  -Dsonar.host.url=http://127.0.0.1:9026 \\
  -Dsonar.login=6fa9111de5d766671b8d40ab85868996dcc69a08'''
      }
    }

  }
}