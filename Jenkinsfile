pipeline {
    agent any
    stages {
        stage('Build') {
			//input {
			//	message "Should we continue?"
            //    ok "Yes, we should."
            //    submitter "alice,bob"
            //    parameters {
			//		string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            //    }
            //}
            when {
				//echo "${params.branchName}"
				//echo "${branch}"
				expression { ${params.branchName} ==~ /(production|staging)/ }
				//${params.branchName} pattern: "^origin/release/d+\.d+\.x", comparator: "REGEXP"
			}
            steps {
				echo "User selected ${params.branchName}"
                //sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}