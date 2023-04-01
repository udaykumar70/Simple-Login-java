pipeline {
   agent { label 'JDK11' }
   options { 
    timeout(time: 1, unit: 'HOURS')
   }
   triggers {
    cron('* */4 * * *')
   }

 stages {
  stage('source code') {
    steps {
        git url: 'https://github.com/udaykumar70/Simple-Login-java.git' , branch: main1
    }
  }
  stage('build') {
   steps {
    sh 'mvn package'
   }
  }
 }
post {
    success {
        echo 'passed'
    }
    unsuccessful {
        echo ' failed'
    }
}
}
