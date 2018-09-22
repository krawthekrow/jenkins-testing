pipeline {
	agent any

	stages {
		stage('Build') {
			steps {
				sh '''
python - <<END
import os
if 'CHANGE_ID' in os.environ and os.environ['CHANGE_AUTHOR'] not in [
	'krawthekrow'
]:
	raise Exception("user not authorized to run jenkins builds");
END
pwd
echo "blah" > hyades-jenkins-test-unique.txt
				'''
			}
		}
	}
}
