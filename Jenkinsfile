pipeline {
  agent {
        docker {
            image 'anthonymonori/android-ci-image' 
            args '-u root:root -e TZ=Asia/Kolkata'
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