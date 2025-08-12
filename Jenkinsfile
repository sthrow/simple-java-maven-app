pipeline {
    agent any
    stages {
        stage('Build') {
            when {
			//	//echo "${params.branchName}"
			//	//echo "${branch}"
				expression { ${params.branchName} ==~ refs/heads/release/1.0.x }
			//	//${params.branchName} pattern: "^origin/release/d+\.d+\.x", comparator: "REGEXP"
			}
            steps {
				echo "User selected ${params.branchName}"
                //sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}