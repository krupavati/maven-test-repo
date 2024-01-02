node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube analysis') {
//   def scannarHome = tool 'Sonarqube-10.1';
       
       steps{
       withSonarQubeEnv('sonarqube-10.1') {
       // If you have configured more than one global server connnection, you can specify its name
//     sh "${scannerHome}/bin/sonar-scanner"
       sh "mvn sonar:sonar"
    }
  }
}
}
