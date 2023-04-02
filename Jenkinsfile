pipeline {
  agent { label 'JDK11 && JDK12' }
  tools {
     maven 'apache-maven-3.6.3'
    }
  options {
    timeout(time: 1, unit: 'HOURS')
  }
  triggers {
    cron('* */4 * * *')
  }
  stages {
    stage('source code') {
        steps {     
      git url: 'https://github.com/udaykumar70/Simple-Login-java.git' , branch: 'main1'
       }
    }
    stage('example') {
        steps {
            sh 'mvn --version'
        }
    }
    stage('build') {
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
