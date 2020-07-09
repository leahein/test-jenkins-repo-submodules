pipeline {
  agent any
  parameters {
    string(
      defaultValue: '',
      description: 'testing parameters',
      name: 'test_submodule'
    )
  }
  stages {
    stage('Build') {
      steps {
        sh "git submodule update --remote ${params.test_submodule}"
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}
