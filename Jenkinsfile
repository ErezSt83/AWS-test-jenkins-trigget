pipeline {
	agent any 
	stages {
		stage('upload to aws') {
			steps  {
				withAWS(region:'us-east-2',credentials:'aws-static') {
					s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:’index.html’, bucket:’myudacityprojectjenkins’)				
				}
			}
		}
	}
}
