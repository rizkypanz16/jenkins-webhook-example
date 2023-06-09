pipeline {
    agent any

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
                sh 'npm install'
                sh 'ls -l'
                echo 'Deploy Prod successfully'
            }
        }
    }
        // Define triggers for the pipeline
    triggers {
        // Webhook trigger for push events
        githubPush()
    }
}
