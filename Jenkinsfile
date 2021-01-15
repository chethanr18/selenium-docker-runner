pipeline{
	agent any
	stages{
		stage("Run Test"){
			steps{
				bat "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Test"){
			steps{
				sh "docker-compose up search-module"
			}
		}
		stage("Stop Grid") {
			steps {
				bat "docker-compose down"
		}
	}
}
