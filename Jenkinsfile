pipeline {
	agent any
	stages {
		stage("run frontend") {
			steps {
				echo 'executing yarn ... '
				nodejs('Node-10.17') {
					sh 'yarn install'
				}
			}
		}		
		stage("run backend") {
			steps {
				script {
				    def version = sh (
					script: "./gradlew properties -q | grep \"version:\" | awk '{print \$2}'",
					returnStdout: true
				    ).trim()
				    sh "echo Building project in version: $version"

				}
		}
	}
}
