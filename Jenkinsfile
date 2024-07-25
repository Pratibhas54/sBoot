pipeline {

	agent any
	tools {
		maven 'm360'
	}

	stages {
	  stage('build') {
		steps {
		  sh 'mvn install -DskipTests'
		}
	  }

	  
		  
		  post {
				archiveArtifacts artifacts: 'target/**.jar', followSymlinks: false

			}
		}
	  }

}

}
