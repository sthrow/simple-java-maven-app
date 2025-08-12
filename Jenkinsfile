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
            if (${params.branchName} ==~ /(production|staging)/) {
				//echo "${params.branchName}"
				//echo "${branch}"
				//expression { ${params.branchName} ==~ /(production|staging)/ }
				//${params.branchName} pattern: "^origin/release/d+\.d+\.x", comparator: "REGEXP"
				echo "Building release branch ${params.branchName}"
			}
            else {
				echo "User selected ${params.branchName}"
                //sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}