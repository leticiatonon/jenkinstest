pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo Build'
      }
    }
    stage('Backend') {
      parallel {
        stage('Backend') {
          steps {
            sh 'echo Unit'
          }
        }
        stage('Performance') {
          steps {
            sh 'echo Performance'
          }
        }
      }
    }
    stage('Frontend') {
      steps {
        sh 'echo Front'
      }
    }
    stage('Static Analysis') {
      steps {
        sh 'echo Analysis'
      }
    }
    stage('Aproved to Deploy') {
      steps {
        input 'Aprovar Deploy'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo Deploy'
      }
    }
  }
}