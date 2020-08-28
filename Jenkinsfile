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
                        sshagent(['c69260a1-8232-44a5-99df-6209a37018c1']) {
                              cd /var/www/html | sudo git init | sudo git pull https://github.com/ashutoshdubey21/web-demo.git
                        }
                        
                  }
            }
            stage('Deploy') {
                  steps {
                        echo 'successful deployed'
                        
                  }
            }
            
      }
}
