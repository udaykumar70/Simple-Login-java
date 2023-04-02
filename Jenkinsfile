pipeline {
    agent none
    options {
    timeout(time: 1, unit: 'HOURS')
  }
  triggers {
    cron('* */4 * * *')
  }
  stages {
    stage('source code') {
      agent {
        node {
         label 'JDK11'
        }
       }
        steps {     
      git url: 'https://github.com/udaykumar70/Simple-Login-java.git' , branch: 'main1'
       }
   
        steps {
        sh 'mvn package'
    }
   } 
  }
 post {
    always {
        echo "hi done"
    }
    success {
        echo "fineshed"
    }
    unsuccessful {
        echo " failed"
    }
 }
}
