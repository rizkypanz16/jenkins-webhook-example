pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		script {
		    sh '''
			echo "start build.."
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
                script {
		    sh '''
		        echo 'start deploy..'
			pm2 start npm --name "simple-microservice" -- start
                        pm2 list
		    '''
		}
            }
        }
    }

    // Define triggers for the pipeline
    triggers {
        // Webhook trigger for push events
        githubPush()
    }
}
