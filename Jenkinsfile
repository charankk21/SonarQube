pipeline{
   
    agent any
	stages{
	stage('SAST-->SonarQube')
		{
			agent {label 'linagent'}
			options { skipDefaultCheckout() }
			steps{
				sh 'echo hello'
			deleteDir()
			sh 'sudo git clone https://github.com/charankk21/SonarQube.git'
			dir('SonarQube')
			{
				sh 'mvn sonar:sonar -Dsonar.projectKey=SonarTest -Dsonar.host.url=http://localhost:9000 -Dsonar.login=a34771d7e25738d4064a1994a97a58c3a72d2a33'
			}
		}
	}
	}
}
