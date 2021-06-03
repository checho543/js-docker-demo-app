pipeline {
	agent any
	stages {
		stage("run frontend") {
			steps {
				echo 'executing yarm ... '

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
