pipeline {
	agent any
	stages {
		stage("run frontend") {
			steps {
				echo 'executing yarm ... '
				nodejs('Node-10.17') {
					sh 'yarm install'
				}
			}
		}		
		stage("run backend") {
			steps {
				echo 'executing gradle ... '
				withGradle() {
					sh './gradlew -v'
				}
			}
		}
	}
}
