pipeline{
	agent any 
	stages{
		stage("Pull Latest Image"){
			steps{
				sh "docker pull virenderpannu/selenium-docker"
			}
		}
		stage("Start Grid"){
			steps{
				sh "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Tests"){
			steps{
				sh "docker-compose up google-search-module duckduckgo-search-module"
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
			sh "docker-compose down"
		}
	}
}
