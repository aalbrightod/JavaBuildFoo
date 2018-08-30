pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('SayHello') {
      steps {
        echo 'Hello'
        sh 'java -version '
        echo '"${MY_NAME}"'
      }
    }
  }
  environment {
    MY_NAME = 'The Greatest Foo'
  }
}