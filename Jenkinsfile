pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        cleanWs()
        sh 'ls -a'
      }
    }
    stage('test') {
      steps {
        sh 'python linting.py'
        sh 'python test.py'
      }
    }
  }
}

