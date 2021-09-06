pipeline {
    agent any
    stages {
      stage('Build Stages') {
        agent none
        steps {
        script {
        stage('SCM Checkout') 
	        {
               deleteDir()
               checkout scm 
          }
        stage('Maven Build'){
            withMaven(maven: 'Maven-3.6.0'){
            sh 'mvn install -Dmaven.test.skip=true'
            }
        }
}
}
        }
    }
}
