pipeline {
		agent any
		stages {
	stage('scm') {
	steps {
		git "https://github.com/sandipdabre/JenkinsGitMaven.git"
		}
	}
	stage('Test') {
        steps {
                /* `make check` returns non-zero on test failures,
                * using `true` to allow the Pipeline to continue nonetheless
                */
                sh 'make check || true' 
                junit '**/target/*.xml' 
            }
        }
	stage('junit') {
	steps {
		junit healthScaleFactor: 1.0, testResults: '/var/lib/jenkins/workspace/PipelineCode/*.xml'
		}
	}
}
}
