pipeline {
	agent any
		tools{
			gradle 'GRADLE'
			
			jdk 'JDK'
			}
			
			stages{
			stage('Checkout'){
				steps{
					git branch: 'master' , url: 'https://github.com/smshubham2005/MyGradleAppDemo.git'
					}
				}
				
				stage('Build'){
				steps{
					sh ' gradle build'
				}
				
				stage('Test'){
				steps{
					sh ' gradle test'
					}
				}
				
				stage('Run Application'){
				steps{
					sh ' gradle run '
					}
				}
			}
			
			post{
				success{
					echo ' Build and Deployment successful'
				}
				failure{
					echo ' Build failed '
				}
			}
		}
