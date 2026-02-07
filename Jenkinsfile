pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        echo 'Checking out source code...'
        checkout scm
      }
    }
    stage('Setup') {
      steps {
        echo 'Setting up environment...'
        sh '''
          python3 -m venv .venv
          source .venv/bin/activate
          pip install -r requirements.txt
        '''
      }
    }
    stage('Build') {
      steps {
        echo 'Building...'
        echo 'Building with love'
      }
    }
    stage('Test') {
      steps {
        echo 'Running pytest...'
        sh '''
          source .venv/bin/activate
          pytest -v
        '''
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying application...'
        echo 'Deployed with care'
      }
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