pipeline {
        agent any
        tools { 
      maven 'MAVEN_HOME' 
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
