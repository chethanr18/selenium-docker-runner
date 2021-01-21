pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
				bat "docker pull chethanr18/selenium-docker-final"
			}
		}
		stage("Run Test"){
			steps{
				bat "docker-compose up"
			}
		}
		stage("Bring Grid Down"){
			steps{
				bat "docker-compose down"
			}
		}
	}
}
