pipeline {
    agent any

    stages {
        
      stage('Check out') {
          steps {
             echo "Checking Bitbucket"
             git credentialsId: 'Github_CredentialID', url: 'https://github.com/MahendraNathReddy446/Sample_Gradle_Build.git'
         }
      } 
      stage('Gradle Build') {
	  steps {
             sh 'gradle –q hello'
             println 'hello'			 
          }  
        }
    }
}
