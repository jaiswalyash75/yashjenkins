pipeline {
  agent {label 'yash-slave'}
  stages {
    stage('cleanup')
    {
    steps {
    cleanWs()
    }
    }
    stage('checkout scm'){
    steps{
     checkout scm
    }
    }
    stage('build') {
      steps {
        sh 'python3 -m virtualenv env'
        sh 'source env/bin/activate'
        sh 'pip3 install -r requirements.txt'
        sh 'python3 linting.py'
      }
    }
    stage('test') {
      steps {
        sh 'python3 test.py'
      }
    }
  }
}

