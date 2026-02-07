pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        echo 'Building with love'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        echo 'Testing with joy'
    }
  }
  
  post {
    success {
      echo 'Pipeline completed successfully!'
    } 
    failure {
      echo 'Pipeline failed. Please check the logs.'
    }
  }
}