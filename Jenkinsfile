// Contribution:
// Added dropdown version selection and conditional test execution
// Shanzay Shah - SSD Lab 12 - Jenkinsfile with Parameters and Conditional Stages

pipeline {
    agent any

    parameters {
        // Parameter type 1: Free text input
        string(
            name: 'VERSION',
            defaultValue: '',
            description: 'version to deploy on prod'
        )

        // Parameter type 2: Dropdown choice
        choice(
            name: 'VERSION',
            choices: ['1.1.0', '1.2.0', '1.3.0'],
            description: 'Select the version to deploy'
        )

        // Parameter type 3: True/False checkbox
        booleanParam(
            name: 'executeTests',
            defaultValue: true,
            description: 'Should tests be executed?'
        )
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building Project'
            }
        }

        stage('Test') {
            when {
                expression {
                    // Only run tests if executeTests parameter is true
                    params.executeTests == true
                }
            }
            steps {
                echo 'Testing Project'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Project'
                // Use the VERSION parameter here
                echo "Deploying version ${params.VERSION}"
            }
        }
    }
}
