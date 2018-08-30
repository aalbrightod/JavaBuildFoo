pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('SayHello') {
      steps {
        echo 'Hello'
        sh 'java -version '
        sh 'echo "I AM... ${MY_NAME}"'
      }
    }
    stage('Deploy') {
      options {
        timeout(time: 30, unit: 'SECONDS')
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
    MY_NAME = 'The Greatest Foo'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'NameVar', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}