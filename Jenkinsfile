pipeline {
   agent any
   stages {
     def mvn = tool 'mymaven';
     stage("build & SonarQube Analysis") {
       agent any
       steps {
         withSonarQubeEnv('sonarqube') {
           sh 'mvn clean package sonar:sonar'
          }
        }
       } 
      }
     }
