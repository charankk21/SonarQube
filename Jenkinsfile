pipeline{
   
    agent {label 'linagent'}
	options {
    skipDefaultCheckout()
  }
    
    stages{
        stage('build'){
        steps{
            sh 'echo hello'
            deleteDir()
            sh 'sudo git clone $gitUrl$'
            
            dir('simple-java-maven-app'){
        	sh 'mvn sonar:sonar -Dsonar.projectKey=SonarTest -Dsonar.host.url=http://localhost:9000 -Dsonar.login=$SonarLogin$'
	        }
            
        }
        }
    }
}