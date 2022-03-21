pipeline {
    agent any
	
    stages {
	
    stage("Checkout code") {
            steps {
                git credentialsId: 'BitBucket_credentials', url: 'https://mahendranathreddypalle@bitbucket.org/pragiti-git/devops/src/master/sap-commerce/.git'
            }
    }
	stage('Compile') {
            steps {
                gradlew('clean', 'classes')
            }
    }
    stage('Unit Tests') {
            steps {
                gradlew('test')
            }
    }
  }
}

def gradlew(String... args) {
    sh "./gradlew ${args.join(' ')} -s"
}
