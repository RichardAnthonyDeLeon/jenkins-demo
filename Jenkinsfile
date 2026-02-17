pipeline {
  agent any

  tools {
    nodejs "NodeJS"   // esto depende de que Jenkins tenga Node configurado
  }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Install') {
      steps {
        sh 'npm ci'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
  }
}