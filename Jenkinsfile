stage('SAST-->SonarQube')
{
	agent {label 'linagent'}
	options { 
        skipDefaultCheckout()
        }
	steps{
		sh 'echo hello'
			deleteDir()
			sh 'sudo git clone https://github.com/charankk21/SonarQube.git'
			dir('SonarQube'){
			sh 'mvn sonar:sonar -Dsonar.projectKey=SonarTest -Dsonar.host.url=http://54.244.41.181:9000 -Dsonar.login=12a39a18aacff4ee3e3c8d425463919a5d5c7fd2'
		}
    }
}
