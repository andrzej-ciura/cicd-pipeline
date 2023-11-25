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
        sh 'sh echo "Test"'
      }
    }

  }
  environment {
    registry = 'aciura86/test'
  }
}