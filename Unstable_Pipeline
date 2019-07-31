pipeline {

    agent any

    stages {
        stage ('Build & Test') {
            steps {
                echo 'Building... Failure here will fail the build'
                script {
                    try {
                        echo 'Running tests...'
                        sh 'exit 1'
                    }
                    catch (exc) {
                        echo 'Testing failed!'
                        currentBuild.result = 'UNSTABLE'
                    }
                }
            }
        }
    }
}
