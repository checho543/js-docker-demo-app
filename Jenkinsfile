pipeline {
	agent any
	stages {
		stage("run frontend") {
			steps {
				echo 'executing yarm ... '
				nodejs('')
			}
		}		
		stage("run backend") {
			steps {
				echo 'executing gradle ... '
			}
		}
	}
}
