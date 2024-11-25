pipeline {
  agent any
  tools {
    maven 'Maven 3.9.9'
  }
  states {
    state('build') {
      steps {
        echo 'compiling sysfoo app...'
        sh 'mvn compile'
      }
    }
    state('test') {
      steps {
        echo 'running unit tests...'
        sh 'mvn clean test'
      }
    }
    state('package') {
      steps {
        echo 'packaging the app...'
        sh 'mvn package -DskipTests'
      }
    }
  }
  post {
    always{
      echo 'This pipeline is completed...'
    }
  }
}
