pipeline{
	agent any
	
	tools{
	maven:'Maven'
	jdk:'JDK'
	}
	stages{
	
	stage 'checkout'{
		steps{
			git branch :'Master',url:'https://github.com/bitcse6c/IBI22CS164-MAVEN.git'
	}
	}
	stage 'build'{
		steps{
			sh 'mvn clean package'
			}
		}
	stage'test'{
		steps{
		sh 'mvn test'
		}	
	}
	stage 'Run Application'{
		steps{
		sh 'java -jar target/maven-1.0-SNAPSHOT.jar'
		}
		}
		}
	post{
		success{
		echo'successfully completed'
		}
		failure{
		echo'failed'
		}
		}
		}
		
