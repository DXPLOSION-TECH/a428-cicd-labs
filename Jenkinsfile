node {
   withDockerContainer (args: '-p 3000:3000', image: 'node:16-buster-slim'){
    stage('Build') 
    {
        sh 'npm cache clean --force'
        sh 'npm install'
    }
    stage('Test')
    { 
        sh './jenkins/scripts/test.sh' 
    }
   }
}