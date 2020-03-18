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
    stage('Test Failure') {
      when {
        expression { "${params.test_submodule}" == "test-jenkins-repo" }
      }
      steps {
        echo "running tests with docker-compose..."
        /* sh "exit 1" */
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}
