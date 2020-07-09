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
        echo "called"
      }
    }
  }
}
