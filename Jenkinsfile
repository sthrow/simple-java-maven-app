pipeline {
	agent any
    stages {
        stage('Build') {
			steps {
				echo "User selected ${params.branchName}"
                //sh 'mvn -B -DskipTests clean package'
                script {
					def branchName = params.branchName
					echo "branchName: ${branchName}"

     				if (branchName ==~ /^refs\/heads\/release\/\d+\.\d+\.x/) {
						echo "matched ${branchName}"
					} else {
						echo "no match for ${branchName}"
					}
				}
            }
        }
    }
}