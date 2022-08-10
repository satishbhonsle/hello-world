def skipRemainingStages = false
pipeline {
  agent any
  environment {
    HOST_NAME= '54.202.249.221'    
  }
  stages {
    stage('Build') {
      steps{
        git branch: $GIT_BRANCH, url: 'https://github.com/satishbhonsle/hello-world.git'
      }
    }
  }
}
