pipeline {
  agent any
  stages {
    stage('clean-up') {
      steps {
        cleanWs()
      }
    }
    stage('checkout-scm') {
      steps {
        checkout scm
      }
    }
    stage('build') {
      steps {
      sh 'python3 -m virtualenv .venv'
      sh 'source .venv/bin/activate'
      sh 'pip3 install -r requirements.txt --user'        sh 'python3 linting.py'
      }
    }
    stage('test') {
      steps {
        sh 'python3 test.py'
      }
    }
    stage('deploy') {
      steps {
        sh 'ls'
      }
    }
  }
}

