pipeline {
  agent any
  stages {
    stage('Development') {
      when {
        branch master
      }
      steps {
        echo 'fetch the code'
      }
    }

    stage('QA') {
      steps {
        echo 'run smoke tests'
        git(url: 'https://github.com/kpkk/EyeAutomation.git', branch: 'master', poll: true)
        bat 'mvn test -DEnvironment=QA'
      }
    }

    stage('deployment') {
      steps {
        echo 'deploy the code'
        echo 'certify the build'
      }
    }

  }
}