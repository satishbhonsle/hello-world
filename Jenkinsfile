pipeline{
  agent any
  stages{
    stage('Git Checkout'){
      steps{
       sh 'git checkout https://github.com/satishbhonsle/hello-world'
      }
    }
    stage('Build repo'){
      steps{
        sh 'docker build -t tomcatimage:v1 .' 
      }
    }    
  }
}
