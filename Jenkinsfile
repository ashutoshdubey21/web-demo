pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
                echo "Initiating a web server"
                sh 'sudo yum install httpd -y'
                sh 'sudo systemctl start httpd'
            }
            post {
                success {
                    echo "Now Archiving the Artifacts...."
                }
            }
        }
    /*
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
