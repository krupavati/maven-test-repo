pipeline {
        agent any
        tools { 
           maven 'mymaven' 
           jdk 'JAVA_HOME' 
    }
        stages {
         
          stage("build & SonarQube Scanner") {
            agent any
            steps {
              withSonarQubeEnv('sonarqube') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
        }
      }
