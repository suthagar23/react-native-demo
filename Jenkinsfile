pipeline {
  agent any
  stage('Prepare') {
    sh "npm install -g yarn"
    sh "yarn install"
  }
  stages {
    stage('Build') {
      steps {
        sh 'yarn install'
      }
    }
  }
}
