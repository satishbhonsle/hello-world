pipeline{
  def ANSIBLE_NODE="54.202.249.221"
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
        def remote = [:]
        remote.host = ansible-server
        remote.name = 'ansadmin'
        withCredentials([sshUserPrivateKey(credentialsId: 'ansadmin', keyFileVariable: '')]) {
          sshcommand remote: remote, command: 'touch /temp/testMe.txt'       
        }
      }
    }    
  }
}
