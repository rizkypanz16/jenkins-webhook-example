pipeline {
    agent any
    environment {
        DB_USER = credentials('admin')
    }
    stages {
        stage('Build') {
            steps {
                // Build steps here
                echo 'Building...'
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
