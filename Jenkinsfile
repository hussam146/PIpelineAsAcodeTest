pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Completed'
      }
    }
    stage('Test Flow') {
      parallel{
        stage('Test Flow'){
          steps{
            echo 'Test Flow entered'
          }
        }
        stage('Test1'){
          steps {
            echo 'Test1 completed'
          }   
        }
      }
    }
  }
}