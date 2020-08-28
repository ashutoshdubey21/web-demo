pipeline {
      agent any
      stages {
            stage('Init') {
                  steps {
                        echo 'Hi, this is Ashutosh from giit'
                        echo 'We are Starting the Testing'
                  }
            }
            stage('Build') {
                  steps {
                        echo 'initializing the git repo. in httpd web server'
                        sh label: 'demo', script: '''cd /var/www/html/
                        git init
                        git pull https://github.com/ashutoshdubey21/web-demo.git'''
                        
                  }
            }
            stage('Deploy') {
                  steps {
                        echo 'Deploying the test website'
                        
                  }
            }
            
      }
}
