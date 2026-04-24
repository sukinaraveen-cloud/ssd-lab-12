pipeline {
    agent any

    tools {
        // 'Maven' here must EXACTLY match the name you set in Jenkins Tools config
        maven 'Maven'
    }

    environment {
        NEW_VERSION = '1.3.0'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
                echo "Building version ${NEW_VERSION}"

                // This runs the Maven install command
                // Use sh for Linux/Mac, bat for Windows
                sh "mvn install"       // Linux / Mac
                // bat 'mvn install'   // Windows — uncomment this line if on Windows
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
}
