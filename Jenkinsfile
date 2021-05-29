pipeline {
		agent any
		stages {
	stage('scm') {
	steps {
		git "https://github.com/sandipdabre/JenkinsGitMaven.git"
		}
	}
	stage('junit') {
	steps {
		junit healthScaleFactor: 1.0, testResults: '**////*.xml'
		}
	}
}
}
