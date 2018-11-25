pipeline {
	agent any
	tools {
    	maven 'Maven360'
    	jdk 'jdk11'
  	}
	stages {
		stage('Build') {
			steps {
				sh 'mvn clean package'
			}
			steps {
				sh 'docker build . -t tomcatwebapp:${env.BUILD_ID}
			}
		}
	}
}