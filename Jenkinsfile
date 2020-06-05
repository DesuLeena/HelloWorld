pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'checkout'
      }
    }

    stage('allocate node') {
      steps {
        node(label: 'master')
      }
    }

    stage('build') {
      steps {
        bat 'HelloWorldTest.bat'
      }
    }

  }
}