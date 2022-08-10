def skipRemainingStages = false
pipeline {
  agent any
  environment {
    HOST_NAME= '54.202.249.221'    
  }
  stages {
    stage('Build') {
      steps{
        sh 'echo $HOST_NAME'
      }
    }
  }
}
