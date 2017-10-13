pipeline {
  agent any
  stages {
    stage('start') {
      steps {
        echo 'ok'
      }
    }
    stage('running') {
      parallel {
        stage('run script') {
          steps {
            sh '''echo "hello"
exit 1'''
          }
        }
        stage('run passes') {
          steps {
            sh 'echo "passes"'
          }
        }
      }
    }
    stage('') {
      steps {
        echo 'finished'
      }
    }
  }
  environment {
    start = 'ok'
  }
}