pipeline{
    tools { 
      maven 'maven3' 
  }
  agent any
    environment {
        registry = "923770093922.dkr.ecr.us-east-1.amazonaws.com/myrepo"
    }
    stages {
         stage('Cloning Git') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/sarithabora2246/mynewspringboot.git']]])     
            }
        }
      stage ('Build') {
          steps {
            sh 'mvn clean install'           
            }
      }
    }
}