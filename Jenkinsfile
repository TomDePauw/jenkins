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
        sh '''print "hello"
exit 1'''
      }
    }
  }
  environment {
    start = 'ok'
  }
}