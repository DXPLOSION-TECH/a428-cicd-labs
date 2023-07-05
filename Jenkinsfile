node
{
    withDockerContainer(args:'-p 3000:3000', image:'node:16-buster-slim')
    {
        checkout (scm)
        stage('Build')
        {
            sh 'npm install'
            //sh 'rm -rf node_modules && npm install'
        }
        stage('Test')
        {
             sh './jenkins/scripts/test.sh' 
        }

        stage('Manual Approval')
        {
            input message: "Lanjutkan ke tahap Deploy?"
        }
        stage('Deploy')
        {
              sh './jenkins/scripts/deliver.sh' 
              sleep(time: 1, unit: 'MINUTES')
              sh './jenkins/scripts/kill.sh' 
        }
    
    }
}
         