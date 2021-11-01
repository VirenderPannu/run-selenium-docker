pipeline{
	agent any 
	stages{
		stage("Bring Grid up and Run Tests"){
			steps{
				sh "docker-compose up"
			}
		}
		stage("Bring Grid down"){
			steps{
				sh "docker-compose down"
			}
		}
	}
}