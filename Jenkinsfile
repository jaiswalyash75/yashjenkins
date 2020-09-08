pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        cleanWs()
        sh 'python3 -m virtualenv env'
        sh 'source env/bin/activate'
        sh 'pip install -r requirements.txt'
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

