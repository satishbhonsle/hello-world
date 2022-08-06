pipeline{
  agent any
  stages{
    stage('Git Checkout'){
      steps{
        echo ' Git checkout'
      }
    }
    stage('Build repo'){
      steps{
        sh 'docker build -t tomcatimage:v2 .' 
      }
    }    
  }
}
