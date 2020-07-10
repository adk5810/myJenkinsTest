pipeline {
	agent any
	stages {
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
