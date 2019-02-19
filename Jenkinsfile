pipeline {
  agent {
        docker {
            image 'node:8' 
            args '-u root:root'
        }
    }
     environment {
        HOME = '.'
    }
  stages {
    stage("Install npm modules") {
      steps {
        sh 'yarn'
      }
    }

    stage("Running Tests") {
      steps {
        sh 'yarn test'
      }
    }


    stage('Branch Develop'){
      when {
        branch 'develop'
      }
      steps {
          echo "develop"
      }
    }

    stage("Clean Workspace") {
      steps{
        cleanWs()
      }
    }
  }
}