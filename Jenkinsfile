pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'checkout'
      }
    }

    stage('build') {
      steps {
        bat 'HelloWorldTest.bat'
      }
    }

  }
}