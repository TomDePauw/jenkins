pipeline {
  agent any
  stages {
    stage('start') {
      steps {
        echo 'ok'
      }
    }
    stage('run script') {
      steps {
        sh '''echo "hello"
exit 1'''
      }
    }
  }
  environment {
    start = 'ok'
  }
}