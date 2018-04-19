pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello World!'
        echo "Hello ${MY_NAME}!"
      }
    }
  }
  environment {
    MY_NAME = 'Mrinal'
  }
}