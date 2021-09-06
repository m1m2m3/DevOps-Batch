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
            withMaven(maven: 'mymaven'){
            sh 'mvn install -Dmaven.test.skip=true'
            }
        }
}
}
        }
    }
}
