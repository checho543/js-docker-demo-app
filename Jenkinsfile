pipeline {
	agent any
    parameters { 
        choice(name: 'Version', choices: ['1.1.0', '1.1.2', '1.1.5'], description: '')
        booleanParam(name: ' executeTests', defaultValue: true, description: '')
    }
	stages {
		stage("build") {
			steps {
				echo 'building the application ... '
			}
		}		
		stage("test") {
            when {
                expression {
                    params.executeTests == true
                }
            }
			steps {
				echo 'testing the application ... '
			}
		}
		stage("deploy") {
			steps {
				echo 'deploying the application ... '
                echo "deploying version ${params.Version}"
			}
		}
	}
}
