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
  }
  environment {
    MY_NAME = 'The Greatest Foo'
    TEST_USER = credentials('test-user')
  }
}