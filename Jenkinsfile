node('JDK8') {
   stage('source code') {
    git branch: 'main', url: 'https://github.com/udaykumar70/Simple-Login-java.git' 
 }
  stage('build the code execute shell') {
    sh 'mvn package'
 }
}
