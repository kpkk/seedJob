pipeline {
  agent any
  stages {
    stage('Development') {
      steps {
        echo 'fetch the code'
      }
    }

    stage('QA') {
      steps {
        echo 'run smoke tests'
      }
    }

    stage('deployment') {
      steps {
        echo 'deploy the code'
      }
    }

  }
}