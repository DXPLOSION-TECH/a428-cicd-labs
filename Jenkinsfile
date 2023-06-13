node {
    stage('Install')
    {
        sh 'npm install'    
    }
    stage('Build') 
    {
        sh 'npm build'
    }
    stage('Test')
    { 
        sh './jenkins/scripts/test.sh' 
    }
   
}