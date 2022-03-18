pipeline {
    agent any

    stages {
        
      stage('Check out') {
          steps {
             echo "Checking Bitbucket"
             git credentialsId: 'Github_CredentialID', url: 'https://github.com/MahendraNathReddy446/Sample_Gradle_Build.git'
         }
      } 
	  stage('Compile') { // Compile and do unit testing
      tools {
        //gradle 'gradle4'
      }
      steps {
        // run Gradle to execute compile and unit testing
        //sh 'gradle clean compileJava test'
      }
      /*stage('Gradle Build') {
	  steps {
             sh "./gradlew"
             println 'hello'			 
          }  
        }*/
	 }
    }
}
