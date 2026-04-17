pipeline {
	agent any
	
	tools {
		gradle 'Gradle'
		jdk 'JDK'
	}
	
	stages {
		stage('Checkout') {
			steps {
				git branch:'master', url: 'https://github.com/mithun2311/MyGradleTest01'
			}
		}
		
		stage('Build') {
			steps {
				sh 'gradle build'
			}
		}
		
		stage('Test') {
			steps {
				sh 'gradle test'
			}
		}
		
		stage('Run Application') {
			steps {
				sh 'gradle run'
			}
		}
		
	}
	post {
		success {
			echo 'Build and Deployment Successfull'
		}
		failure {
			echo 'Build Failed'
		}
	}
} 
