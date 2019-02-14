pipeline {
  agent {
        docker {
            image 'node:8-alpine'
            args '-p 3000:3000'
        }
    }
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
