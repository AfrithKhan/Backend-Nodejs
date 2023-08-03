pipeline {
  agent any
    
    
  stages {

    stage('SSH into remote instance') {
      steps {
          script {
              // Define the SSH credentials ID configured in Jenkins
              def sshCredentialsId = '09dd4efb-df5e-471b-b6cb-0e9f4aafe54d'
              
              // Remote SSH commands
              def remoteCommands = [
                  "ssh root@35.154.35.30 'cd /home/ubuntu/Backend-Nodejs && docker build -t node .'",
                  "ssh root@35.154.35.30 'docker stop node && docker rm node'"
                  "ssh root@35.154.35.30 'docker run --name node -d -p 3333:3333 node'",                  
                  // Add more remote commands here if needed
              ]
              
              // Use the SSH Agent to run the remote commands
              sshagent(credentials: [sshCredentialsId]) {
                  for (def command in remoteCommands) {
                      sh command
                  }
              }
          }
      }
    }
        

  }
}
