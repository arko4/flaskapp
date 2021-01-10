pipeline {

  environment {
    imagename = "devopstestaccount/api"
    registryCredential = 'devopstestaccount-id'
    dockerImage = ''
  }

  agent label 'dockerhost-label'

  stages {
    stage('Build') {
      steps{
        script {
          dockerImage = docker.build imagename
        }
      }
    }
  }
}
