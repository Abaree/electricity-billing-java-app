pipeline {
  agent any
    stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage ('Static Application Security Testing = SAST') {
		steps {
		withSonarQubeEnv('sona-olowo') {
			sh 'mvn sonar:sonar'
			sh 'cat target/sonar/report-task.txt'
		       }
		}
	}
  }
}