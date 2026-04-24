def flag = true    // This is a variable defined outside the pipeline

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
            }
        }

        stage('Test') {
            when {
                expression {
                    flag == false    // Test stage ONLY runs if flag equals false
                }
            }
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
}
