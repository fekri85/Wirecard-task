pipeline {
    agent any
    options {
        skipDefaultCheckout(true)
    }
 
    stages {
        stage('Git') {
            steps {
                echo '> Check the Git'
                checkout scm
            }
        }
	}
        stage('Deploy tomcatserver') {
            steps {
                echo '> installing the tomcatserver'
                ansiblePlaybook(
				    ansiblePlaybook colorized: true, 
					credentialsId: 'ssh-jenkins',
                    inventory: 'Provision/hosts.yaml',
                    playbook: 'Provision/tomcatserver.yaml'
					sudo: true,
					sudoUser: 'jenkins'
                )
            }
        }
}