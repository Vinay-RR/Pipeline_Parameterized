pipeline {
  agent any
  parameters {
  string defaultValue: 'TEST', description: 'Environment to deploy the application', name: 'ENV', trim: true
   choice choices: ['main', 'master'], description: 'environment to deploy application', name: 'BRANCH'
}	
environment {
       DEPLOY_BRANCH = "$BRANCH"
	   DEPLOY_ENV = "$ENV"
	   }
   stages {
    stage ('BUILD') {
      steps {
	  echo "Deploying to ${params.ENV}"
	  echo "Code from ${params.BRANCH}"
        sh '''
		sleep 5
		echo deploying to ${BRANCH}
		echo code from ${ENV}
		exit 0
		'''
		}
	}
     }
  }
