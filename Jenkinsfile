node('JDK8') {
	stage('SourceCode') {
		// get the code from git repo
	        git branch: 'sprint1_developer', url: 'https://github.com/sanku7668/game-of-life.git'
	}    
	stage('Build the code') {
		sh 'mvn clean package'
	}	
	stage('Archiving and Test Results') {
		junit stdioRetention: '', testResults: '**/surefire-reports/*.xml'	
		archiveArtifacts artifacts: '**/*.war', followSymlinks: false
	}
}
