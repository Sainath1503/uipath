pipeline {
  agent any
  environment {
      MAJOR = '1'
      MINOR = '0'
  }
  stages {
    stage ('Build') {
	  steps {
         UiPathRunJob(
          credentials: UserPass('3CK9qjk3hhTgHjnqeANuUQKRJrklIPTlcmw66qBkVbtXX'),
          failWhenJobFails: true,
          folderName: 'My Workspace',
          orchestratorAddress: 'https://cloud.uipath.com/',
          orchestratorTenant: 'DefaultTenant',
          parametersFilePath: '',
          priority: 'Low',
          processName: 'ProcessA_EnvB',
          resultFilePath: 'project.json',
          strategy: Dynamically(jobsCount: 1, machine: 'TestMachine', user: 'TestUser'), timeout: 3600, waitForJobCompletion: true, traceLevel: 'None'
         )
		}
    }
  }
}