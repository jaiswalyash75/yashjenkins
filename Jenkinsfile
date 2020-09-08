
pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        cleanWs()
        checkout scm
        sh 'python -m virtualenv .venv'
        sh 'source .venv/bin/activate'
        sh 'ls -a'
        sh 'pwd'
        sh 'python3 --version'
        sh 'pip install -r requirements.txt'
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

