pipeline {
 agent none
 stages{
  stage("build and SonarQube Analysis")
  {
   agent any
    steps {
	 withSonarQubeEnv('SonarQube')
	 {
	  sh "mvn clean package sonar:sonar -Dsonar.projectKey=Ashu -Dsonar.projectName='Ashu'"
	 }
	}
  }
 }
}
