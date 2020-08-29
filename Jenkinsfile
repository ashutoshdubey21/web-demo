pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                sh 'git init'
            }
            post {
                success {
                    echo "Now Archiving the Artifacts...."
                    archiveArtifacts artifacts: '**/*'
                }
            }
        }
        stage('Deploy in Staging Environment'){
            steps{
                build job: 'Deploy_Application_Staging_Env'
 
            }
            
        }
    /*
        stage('Deploy to Production'){
            steps{
                timeout(time:5, unit:'DAYS'){
                    input message:'Approve PRODUCTION Deployment?'
                }
                build job: 'Deploy_Application_Prod_Env'
            }
        }
  */
    }
}
