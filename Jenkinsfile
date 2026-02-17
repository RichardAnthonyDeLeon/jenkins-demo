pipeline {
  agent any

  tools {
    nodejs "NodeJs"   // esto depende de que Jenkins tenga Node configurado
  }

  stages {
    stage('Checkout') { //descarga el código del repositorio
      steps {
        checkout scm
      }
    }

    stage('Install') { // instala las dependencias del proyecto
      steps {
        sh 'npm ci'
      }
    }

    stage('Test') { // ejecuta los tests definidos en el proyecto
      steps {
        sh 'npm test'
      }
    }
  }
}