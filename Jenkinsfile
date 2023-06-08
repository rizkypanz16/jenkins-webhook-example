pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		script {
		    sh '''
			echo "start build"
			ls -l
			npm install
			npm run build
			ls -l
		    '''
		}
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
