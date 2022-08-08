pipeline{
//   def remote = [:]
//   remote.host = '54.202.249.221'
//   remote.name = 'ansadmin'  
  agent any
  stages{
    stage('Git Checkout'){
      steps{
        echo ' Git checkout'
        checkout scm
      }
    }
    stage('Build repo'){
      steps{
        withCredentials([sshUserPrivateKey(credentialsId: 'ansadmin', keyFileVariable: '')]) {
          sshcommand remote: remote, command: 'touch /temp/testMe.txt'       
        }
      }
    }    
  }
}
