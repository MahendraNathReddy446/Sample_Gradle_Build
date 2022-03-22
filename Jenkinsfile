pipeline {
    def gradleHome = tool name: "gradle7.3.2"
    agent any

    stages {
        stage("check out SCM"){
           steps {
            git credentialsId: 'Github_CredentialID', url: 'https://github.com/MahendraNathReddy446/Sample_Gradle_Build.git''
            }
		}
        stage('Gradle Build') {
           steps {
            sh "${gradleHome}/bin/gradle build"
            println 'hello'
            }			
        }  
    }
}
