pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build steps here
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                // Test steps here
                echo 'Testing...'
            }
        }

        stage('Deploy') {
            steps {
                // Deployment steps here
                echo 'Deploying...'
            }
        }
    }

    // Define triggers for the pipeline
    triggers {
        // Webhook trigger for push events
        githubPush()
    }
}
