pipeline {
  agent any
  parameters {
    string(
      defaultValue: '',
      description: 'testing parameters',
      name: 'test-submodule'
    )
  stages {
    stage('Build') {
      steps {
        sh "git submodule update --remote ${params.test-submodule}"
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
