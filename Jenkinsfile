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
          stage('test') {
		steps {
		  sh 'mvn test'
		}
	  }
	}
	  
		  
		  post {
			always {
			  archiveArtifacts artifacts: 'target/**.jar', followSymlinks: false

			
			}
            }

}
