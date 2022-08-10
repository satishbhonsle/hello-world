def skipRemainingStages = false
pipeline {
  agent any
  environment {
    HOST_NAME= '54.202.249.221'    
  }
  stages {
    stage('SCM Checkout') {
      steps{
        checkout(
                [
                    $class: 'GitSCM',
                    branches: [[name: "$GIT_BRANCH"]],
                    doGenerateSubmoduleConfigurations: false,
                    submoduleCfg: [],
                    userRemoteConfigs: [[credentialsId: "",
                    url: "$GIT_URL"]]
                ]
         )
      }
    }
    stage('Dokcer build') {
      steps{
        sh 'docker build -t tomcatimage:v1 .'
      }
    }
  }
}
