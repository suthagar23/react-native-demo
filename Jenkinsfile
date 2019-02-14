pipeline {
  agent any
  tools {nodejs "node"}
  stages {
    stage('Prepare') {
      steps {
        sh "npm install -g yarn"
        sh "yarn install"
      }
    }
    stage('Build') {
      steps {
        sh 'yarn install'
      }
    }
  }
}
