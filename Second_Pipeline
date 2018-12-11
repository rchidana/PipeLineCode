pipeline {
    agent any
	
    stages {
        stage('Git-Checkout') {
            steps {
                    echo "Checking out from Git Repo";
                    /* Put in the actual Code for checking out code from your Git Repo here */
            }
        }
        
        stage('Build') {
            steps {
                    echo "Building the checked-out project!";
                     /* Put in the actual Code for Executing Build.bat file from your Git Repo here */
            }
        }
        
        stage('Unit-Test') {
            steps {
                    echo "Running JUnit Tests"; 
                    /* Put in the actual Code for Executing Unit.bat file from your Git Repo here */
             }
        }
        
        stage('Quality-Gate') {
            steps {
                  echo "Verifying Quality Gates";
                  /* Put in the actual Code for Executing Quality.bat file from your Git Repo here */

            }
        }
        
		stage('Deploy') {
            steps {
                  echo "Deploying to Stage Environment for more tests!";
                  /* Put in the actual Code for Executing Deploy.bat file from your Git Repo here */
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
