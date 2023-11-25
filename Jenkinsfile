pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        script {
          checkout scm
        }

      }
    }

    stage('Build') {
      steps {
        sh 'scripts/build.sh'
      }
    }

  }
  environment {
    registry = 'aciura86/test'
  }
}