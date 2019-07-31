pipeline {
  agent any
  environment {
    registry = 'anchorecontainerregistry001.azurecr.io'
    registryCredential = 'azure'
  }
  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/jyankel/anchore-jenkins-pipeline.git'
      }
    }
    stage('Building image') {
      steps {
        script {
         docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }
  }
}
