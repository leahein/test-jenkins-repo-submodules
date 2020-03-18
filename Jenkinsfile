pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh "git submodule update --remote"

      }
    }
    stage('Test Failure') {
      steps {
        echo 'Testing..'
        sh "exit 1"
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}
