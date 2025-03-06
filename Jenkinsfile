pipeline {
 agent none
 stages{
  stage("build and SonarQube Analysis")
  {
   agent any
    steps {
	 withSonarQubeEnv('SonarQube')
	 {
	 mvn clean verify sonar:sonar \
  -Dsonar.projectKey=Ashu \
  -Dsonar.projectName='Ashu' \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.token=sqp_3e9ef2cb577467b3b6c386229a15f611a489598c
	}
  }
 }
}
