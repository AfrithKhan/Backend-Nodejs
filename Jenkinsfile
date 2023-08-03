pipeline {
  agent any
    
    
  stages {
        
    // stage('Git') {
    //   steps {
    //     git 'git@github.com:AfrithKhan/Backend-Nodejs.git'
    //   }
    // }#
     
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }  
    
            
    stage('Test') {
      steps {
        sh 'node test'
      }
    }
  }
}
