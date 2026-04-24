pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing Project'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Project'
            }
        }
    }

    post {
        always {
            // This runs every time, whether build passed or failed
            echo 'Post build condition running'
        }
        failure {
            // This only runs if the build FAILED
            echo 'Post Action if Build Failed'
        }
    }
}
