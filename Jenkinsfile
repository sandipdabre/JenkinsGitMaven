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
		junit healthScaleFactor: 1.0, testResults: '/var/lib/jenkins/workspace/PipelineCode/*.xml'
		}
	}
}
}
