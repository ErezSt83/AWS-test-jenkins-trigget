pipeline {
	agent any 
	stages {
		stage('upload to aws') {
			steps  {
				withAWS(region:'us-west-2', credentials: 'Jenkins') {
					s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’myudacityprojectjenkins’)				
				}
			}
		}
	}
}
