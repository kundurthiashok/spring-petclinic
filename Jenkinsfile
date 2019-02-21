pipeline{
    agent any
     stages{
        
        stage("GIT clone or PULL"){
            steps {
                
                git 'https://github.com/kundurthiashok/spring-petclinic.git'
                
            }
		}
		    stage("MAVEN"){
                steps{
                    sh label: '', script: 'mvn clean install'
                }
			}
				
            stage("Publish"){
                steps{
                    archiveArtifacts 'target/spring-petclinic-2.1.0.BUILD-SNAPSHOT.jar'
                    junit 'targets/surefire-reports/*.xml'
                }
            }
	}
	}
	
  
