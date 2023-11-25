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

    stage('Test') {
      steps {
        sh 'scripts/test.sh'
      }
    }

    stage('Build Docker Image') {
      steps {
        script {
          def customImage = docker.build("${registry}:${env.BUILD_ID}")
        }

      }
    }

  }
  environment {
    registry = 'aciura86/test'
  }
}