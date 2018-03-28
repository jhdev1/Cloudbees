pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo \'test\''
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo \'test\''
          }
        }
        stage('') {
          steps {
            sh 'echo \'test2\''
          }
        }
      }
    }
  }
}