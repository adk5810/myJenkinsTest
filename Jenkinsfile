pipeline {
	agent any
	tools {
		maven "Maven"
	}
	stages {
		stage ('build') {
			steps {
			    echo "build"
			    sh mvn compile
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
	post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}
