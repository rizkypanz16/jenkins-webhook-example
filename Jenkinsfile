pipeline {
    agent any
    environment {
        DB_USER = credentials('admin')
        DB_PASS = credentials('ijinmasuk')
    }
    stages {
        stage('Build') {
            steps {
                // Build steps here
                echo 'Building...'
                echo '$DB_USER & $DB_PASS'
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
