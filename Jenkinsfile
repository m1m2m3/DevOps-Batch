pipeline {

    agent any
    tools {
        maven 'Maven_3.5.2' 
    }
	stages {
		stage('SCM checkout') {
			steps { 
			git "https://github.com/m1m2m3/DevOps-Batch.git"
			} 
		}
	}
    stages {
        stage('Compile stage') {
            steps {
                bat "mvn clean compile" 
        }
    }

         stage('testing stage') {
             steps {
                bat "mvn test"
        }
    }

          stage('deployment stage') {
              steps {
                bat "mvn deploy"
        }
    }

  }

}
