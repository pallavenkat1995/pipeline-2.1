pipeline {
	agent any
	tools{ 
            jdk 'jdk 8u221'
          }
    stages {     
        	stage ('Initialize') {
                 steps {
                     sh '''
                          echo "PATH = ${PATH}"
                          echo "M2_HOME = ${M2_HOME}"
                         ''' 
                         }
		stage('---clean---'){
			steps {
				sh "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				sh "mvn test"
			}
		}
		stage('---package---')
			steps {
				sh "mvn package"
			}
		}
	}
}
