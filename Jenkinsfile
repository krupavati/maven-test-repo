pipeline {
   agent none
   stages {

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
