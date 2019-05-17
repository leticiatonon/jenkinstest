pipeline {
  agent any
  stages {
    stage('Inicial') {
      agent any
      steps {
        echo 'Inicio dos Testes'
      }
    }
    stage('Docker') {
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