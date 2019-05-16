pipeline {
  agent any
  stages {
    stage('Inicial') {
      agent any
      steps {
        echo 'Inicio do Processo'
      }
    }
    stage('') {
      agent {
        docker {
          image 'nginx'
        }

      }
      steps {
        echo 'Docker'
      }
    }
  }
}