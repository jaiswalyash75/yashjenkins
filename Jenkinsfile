
pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        cleanWs()
        checkout scm
        sh 'python3 -m virtualenv .venv'
        sh 'source .venv/bin/activate'
        sh 'ls -a'
        sh 'pwd'
        sh 'python3 --version'
        sh 'pip3 install -r requirements.txt --user'
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

