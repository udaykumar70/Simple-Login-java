pipeline {
   agent { label 'JDK11' } 
   stages {
      stage('source code') {
        steps {
          git branch: 'main', url: 'https://github.com/udaykumar70/Simple-Login-java.git'    
          }

        }
      stage('build') {
        steps {
         sh 'mvn package'
}
}

}

}

