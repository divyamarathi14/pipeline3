
pipeline {
  agent { label 'agent2' }  
	stages {
		stage('BUILD') { 
      agent { label 'master' }
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the first stage: BUILD
				'''
			}	
		}
		
		stage('TEST') { 
      agent { label 'agent1' }     
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the second stage: TEST
				'''
			}	
		}
		
		stage('DEPLOY') { 
      agent { label 'agent2' }
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the third stage: DEPLOY
				'''
			}	
		}
	}
}
