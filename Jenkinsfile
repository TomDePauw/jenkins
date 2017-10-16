pipeline {
  agent any
  stages {
    stage('start') {
      steps {
        sh '''if ssh adhese@hugo stat ~/docker/adhese/_lifecycle/env.sh \\> /dev/null 2\\>\\&1
            then
                    echo "File exists"
                    exit 0;
            else
                    echo "File does not exist"
                    exit 1;

fi'''
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
    stage('error') {
      steps {
        echo 'finished'
      }
    }
  }
  environment {
    start = 'ok'
  }
}