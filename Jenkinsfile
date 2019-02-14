pipeline {
  agent any
  stages {
    stage('Prepare') {
      sh "npm install -g yarn"
      sh "yarn install"
    }
    stage('Build') {
      steps {
        sh 'yarn install'
      }
    }
  }
}
