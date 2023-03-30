node('JDK8') {
   stage('Source code') {
    git branch: 'main', url: 'https://github.com/udaykumar70/Simple-Login-java.git' 
 }
  stage('Build the code execute shell') {
    sh 'mvn package'
 }
}
