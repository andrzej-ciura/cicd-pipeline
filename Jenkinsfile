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

  }
  environment {
    registry = 'aciura86/test'
  }
}