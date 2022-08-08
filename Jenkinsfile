pipeline{
  def ANSIBLE_NODE="54.202.249.221"
  agent $ANSIBLE_NODE
  stages{
    stage('Git Checkout'){
      steps{
        echo ' Git checkout'
        checkout scm
      }
    }
    stage('Build repo'){
      steps{
        docker.build(tomcatimage:v2) 
      }
    }    
  }
}
