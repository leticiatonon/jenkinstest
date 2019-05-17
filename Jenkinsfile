pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/mauriciopgomes/jenkinstest', branch: 'master', poll: true)
      }
    }
  }
}