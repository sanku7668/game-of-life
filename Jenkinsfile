
pipeline {
	agent { label 'JDK8' }
	stages {
		stage('SourceCode'){
	             steps {
			   git branch: 'sprint1_developer', url: 'https://github.com/sanku7668/game-of-life.git'
 	 	   }
		} 
		stage('Build th code') {
		     steps {
			   sh 'mvn clean package'
                   }	
                }
		stage('Archiving and Test Results') {
		     steps {
			   junit stdioRetention: '', testResults: '**/surefire-reports/*.xml'
			   archiveArtifacts artifacts: '**/*.war', followSymlinks: false
 		   }
		}		 
			
	}	
   }

