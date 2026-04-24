pipeline {
    agent any

    environment {
        // Define your custom variables here
        // They can be used by ALL stages below
        NEW_VERSION = '1.3.0'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                // To use an environment variable, wrap it in ${} inside double quotes
                echo "Building version ${NEW_VERSION}"
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
                echo "Deploying version ${NEW_VERSION}"
            }
        }
    }
}
