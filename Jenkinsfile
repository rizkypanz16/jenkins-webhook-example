pipeline {
    agent any

    // Define triggers for the pipeline
    triggers {
        // Webhook trigger for push events
        githubPush()
    }

    stages {
        stage('Dev Environment') {
            agent {
                label 'panzdocker-1'
            }
            when {
                branch 'dev'
            }
            steps {
                sh 'ls -l'
                echo 'Start Deploy Dev'
                sh 'npm install'
                sh 'pm2 start npm --name "simple-microservice-dev" -- start'
                sh 'pm2 list'
                echo 'Deploy Dev successfully'
            }
        }
        stage('Prod Environment') {
            agent {
                label 'panzdocker-2'
            }
            when {
                branch 'prod'
            }
            steps {
                echo 'Start Deploying app'
                sh 'ls -l'
                echo 'Start Deploy Prod'
                echo 'Deploy Prod successfully'
            }
        }
    }
}
