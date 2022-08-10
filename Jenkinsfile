def skipRemainingStages = false
pipeline {
  agent any
  environment {
    HOST_NAME= '54.202.249.221'    
  }
  stages {
    stage('Build') {
      steps{
        checkout(
                [
                    $class: 'GitSCM',
                    branches: [[name: "*/PR-*"]],
                    doGenerateSubmoduleConfigurations: false,
                    submoduleCfg: [],
                    userRemoteConfigs: [[credentialsId: "",
                    url: "$GIT_URL"]]
                ]
         )
      }
    }
  }
}
