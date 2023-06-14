node {
   withDockerContainer (args: '-p 3000:3000', image: 'node:16-buster-slim'){
    stage('Build') 
    {
        sh 'cp /home/Documents/a428-cicd-labs/package.json /var/jenkins_home/workspace/submission-cicd-pipeline-andrean_candra_w'
        sh 'npm install'
    }
    stage('Test')
    { 
        sh '$(WORKSPACE)/jenkins/scripts/test.sh' 
    }
   }
}