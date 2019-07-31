pipeline {
  agent any
  stages {
    stage('Building') {
      steps {
        sh 'docker.build registry + ":$BUILD_NUMBER"'
      }
    }
  }
  environment {
    registry = 'anchorecontainerregistry001.azurecr.io'
    registryCredential = 'azure'
  }
}