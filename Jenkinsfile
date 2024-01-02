pipeline {
   agent none
   stages {

     stage("build & SonarQube Analysis") {
       agent any
       steps {   
         withSonarQubeEnv('sonarqube') {
           sh 'maven clean package sonar:sonar'
          }
        }
       } 
      }
     }
