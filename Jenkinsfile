pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o task5 main/task5.cpp'
        echo 'Build Successful!'
      }
    }
    stage('Test') {
      steps {
        sh './task5'
        echo 'Test Successful!'
      }
    }
    stage('Deploy') {
      steps {            
        echo 'Successfully deployed!'
      }
    }
  }
  post {
    failure {
      sh 'nonexistent_command' // Intentional Error
      echo 'Pipeline Failed!'
    }
  }
}
