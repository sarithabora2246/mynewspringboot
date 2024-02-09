pipeline{
     agent any
    tools { 
      maven 'maven3' 
    }
    stages {
         stage('Cloning Git') {
            steps {
                 git branch: 'main', url: 'https://github.com/sarithabora2246/helloworld.git'   
            }
        }
      stage('Pull Changes') {
      steps {
        sh 'git pull origin main'
      }
    }
    stage('Build') {
      steps {
        echo '<--------------- Building --------------->'
        sh 'printenv'
        sh 'mvn clean install'
        echo '<------------- Build completed --------------->'
      }
    }
    }
}