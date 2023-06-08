pipeline {
    agent any
    environment {
        DB_USER = 'admin'
        DB_PASS = 'ijinmasuk'
    }
    stages {
        stage('Build') {
            steps {
                // Build steps here
                echo 'Building...'
                sh("echo ${DB_USER} & ${DB_PASS}")
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
