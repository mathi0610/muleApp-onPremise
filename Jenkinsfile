pipeline {
    
    agent any
    
    environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerhub')
	}
    
    stages {
        
        stage('login'){
            steps {
                bat 'echo 'MT9Ai1H97' | docker login -u mathi610 --password-stdin'
            }
        }
        
        stage('Build') {
            steps {
		    bat 'kubectl apply -f k8-multimule.yaml'                
            }
        }
        
    }
}
