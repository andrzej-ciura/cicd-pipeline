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
        sh "chmod +x -R ${env.WORKSPACE}"
        sh 'scripts/build.sh'
      }
    }

  }
  environment {
    registry = 'aciura86/test'
  }
}
