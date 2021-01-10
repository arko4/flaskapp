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
#    stage('Push') {
#      steps{
#        script {
#          docker.withRegistry( '', registryCredential ) {
#            dockerImage.push("$BUILD_NUMBER")
#             dockerImage.push('latest')
#
#          }
#        }
#      }
#    }
#    stage('Clean') {
#      steps{
#        sh "docker rmi $imagename:$BUILD_NUMBER"
#         sh "docker rmi $imagename:latest"
#
#      }
#    }
#  }
}
