pipeline {
   agent none
   stages {

     stage("build & SonarQube Analysis") {
       agent any
       steps {   
         withSonarQubeEnv('sonar_server') {
           sh 'mvn clean package sonar:sonar'
          }
        }
       } 
      }
     }
