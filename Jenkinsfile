pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Build'
          }
        }
        stage('Git') {
          steps {
            git(url: 'https://github.com/mauriciopgomes/jenkinstest', branch: 'master', poll: true)
          }
        }
        stage('Nginx') {
          agent {
            docker {
              image 'nginx'
            }

          }
          steps {
            echo 'Nginx'
          }
        }
      }
    }
    stage('Unit Test') {
      steps {
        echo 'Test'
      }
    }
    stage('Dev') {
      steps {
        echo 'Test Environment'
      }
    }
  }
}