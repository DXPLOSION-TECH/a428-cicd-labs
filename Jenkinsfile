node {
   withDockerContainer (args: '-p 3001:3001', image: 'node:16-buster-slim'){
    stage('Build') 
    {
        sh 'npm install'
    }
    stage('Test')
    { 
        sh './jenkins/scripts/test.sh' 
    }
   }
}