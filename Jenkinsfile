pipeline {
    agent any

    stages {
        stage("check out SCM"){
		    steps {
            git credentialsId: 'Github_CredentialID', url: 'https://github.com/MahendraNathReddy446/Sample_Gradle_Build.git''
            }
		}
        stage('Build') {
            steps {
                sh 'make' 
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }  
    }
}
