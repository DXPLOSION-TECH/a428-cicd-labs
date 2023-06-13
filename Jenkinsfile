node {
   withDockerContainer (args: '-p 3001:3001', image: 'node:16-buster-slim'){
    stage('Build') 
    {
        sh 'npm cache clean --force'
        sh 'npm build'
    }
    stage('Test')
    { 
        sh './jenkins/scripts/test.sh' 
    }
   }
}