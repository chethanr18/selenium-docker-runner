pipeline{
	agent any
	stages{
		stage("Pull Latest Image "){
			steps{
				bat "docker pull chethanr18/selenium-docker-final"
			}
		}
		stage("Start Grid"){
			steps{
				bat "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Test"){
			steps{
				bat "docker-compose up search-module"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
			bat "docker-compose down"
		}
	}
}
