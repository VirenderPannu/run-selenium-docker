pipeline{
	agent any 
	stages{
		stage("Start Grid"){
			steps{
				sh "docker-compose up -d hub chrome firefox --no-colors"
			}
		}
		stage("Run Tests"){
			steps{
				sh "docker-compose up search-module book-flight-module --no-colors"
			}
		}
		stage("Bring Grid down"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}
