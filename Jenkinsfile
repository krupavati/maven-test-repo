pipeline {
   agent any
   stages {

     stage("build & SonarQube Analysis") {
       agent any
       steps {
         def mvn = tool 'mymaven';
         withSonarQubeEnv('sonarqube') {
           sh 'mvn clean package sonar:sonar'
          }
        }
       } 
      }
     }
