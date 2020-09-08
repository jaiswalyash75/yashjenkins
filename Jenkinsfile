
pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        cleanWs()
        checkout scm
        sh 'python3 -m virtualenv env'
        sh 'source env/bin/activate'
        sh 'ls -a'
        sh 'pwd'
        sh 'python3 --version'
        sh 'pip3 install -r requirements.txt'
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

