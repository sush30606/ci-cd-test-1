pipeline {
	agent any

	stages {
		stage('Fetch Code') {

			steps {
			    git branch: 'main', changelog: false, poll: false, url: 'https://github.com/helpingpeopletolearn/ci-cd-test.git'
			}
		}
		stage('Install and configure Apache') {

			steps {
				sh 'sudo apt install apache2 -y'
			}
		}
	   stage('Deploy application') {

			steps {
				sh 'sudo cp -R . /var/www/html/'
			}
		}
	}
}
