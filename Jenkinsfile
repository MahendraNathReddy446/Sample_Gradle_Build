pipeline {
    agent any
	
    stages {
	
    stage("Checkout code") {
            steps {
                git credentialsId: 'Github_CredentialID', url: 'https://github.com/MahendraNathReddy446/Sample_Gradle_Build.git'
            }
    }
	stage('Compile') {
            steps {
                gradlew('clean', 'classes')
            }
    }
    /*stage('Unit Tests') {
            steps {
                gradlew('test')
            }
    }*/
  }
}

def gradlew(String... args) {
    sh "./gradlew ${args.join(' ')} -s"
}
