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
        
         stage('Development Tests') {
         when {
            beforeAgent true
            branch 'development'
         }
         steps {
            echo "Run the development tests!"
         }
      }
      }
    }
  }
}
