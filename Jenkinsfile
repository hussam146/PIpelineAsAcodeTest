pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Completed'
        timeout(time: 5, unit: 'SECONDS') {
          sh 'sleep 3'
        } 
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
    stage('validate'){
      steps{
        input(message: 'Are you sure you want to deploy', ok: 'Yes, I\'m sure')
      }
    }
    stage('Deploy'){
      steps{
        sh 'echo $(date)'
        echo "Deployment completed"
      }
    }
  }
}