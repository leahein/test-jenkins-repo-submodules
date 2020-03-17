pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh "git submodule update --remote"

      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}
