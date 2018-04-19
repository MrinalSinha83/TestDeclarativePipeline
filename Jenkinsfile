pipeline {
  agent any
  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello World!'
        echo "Hello ${MY_NAME}!"
        echo "Hi ${params.Name}!"
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
    stage('Deploy') {
      options {
        timeout(time: 1, unit: 'MINUTES')
      }
      input {
        message 'Should we continue?'
      }
      steps {
        echo 'Continuing with deployment'
      }
    }
  }
  environment {
    MY_NAME = 'Mrinal'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}