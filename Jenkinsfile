pipeline{
	agent any
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master',url:'https://github.com/SUSHMITHA96-87/Gradle81.git'
			}
		}
		stage('Build'){
			steps{
				sh 'gradle build'
			}
		}
		stage('Test'){
			steps{
				sh 'gradle test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'gradle run'
			}
		}
	}
	post{
		success{
			echo 'build and deployed successful!'
		}
		faliure{
			echo 'build failure!'
		}
	}
}
