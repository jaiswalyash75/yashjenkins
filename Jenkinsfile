pipeline {
  agent any
  environment {
    GITHUB_CREDENTIALS=credentials('my-git-creds')
  }
  stages {
    stage('build') {
      steps {
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
  post{
     always {
        cleanWs()
     }
  }
}

