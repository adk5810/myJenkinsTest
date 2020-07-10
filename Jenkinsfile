pipeline {
	agent any
	tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
	stages {
	    stage ('checkout repository') {
	        steps{
	            #git branch: 'dev', credentialsId: '88732a4d-0b04-4fb5-82b5-3648e0879c49', url: 'https://github.com/adk5810/myJenkinsTest.git'
              echo "checkout repository"
	        }
	    }
		stage ('build') {
			steps {
			    echo "build"
			}
		}
		stage ('test: integration-&-quality') {
		    steps {
			echo "test: integration-&-quality"
		    }
		}
		stage ('test: functional') {
		    steps {
			echo "test: functional"
		    }
		}
		stage ('test: load-&-security') {
			steps {
			echo "test: load-&-security"
			}
		}
		stage ('approval') {
			steps {
			echo "approval"
			}
		}
		stage ('deploy:prod') {
			steps {
			    echo "deploy:prod"
			}
		}
	}
}
