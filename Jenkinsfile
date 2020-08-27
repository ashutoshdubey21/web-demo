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
                        echo 'initializing the git repo. in jenkins workspace'
                        sh 'git init'
                        sh 'git pull https://github.com/ashutoshdubey21/web-demo.git'
                  }
            }
            stage('Deploy') {
                  steps {
                        echo "Deploying the test website"
                        sh 'cp -r . /var/www/html'

                  }
            }
            
      }
}
