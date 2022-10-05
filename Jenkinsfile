pipeline {
    
    agent any
    
    environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerhub')
	}
    
    stages {
        
        stage('login'){
            steps {
                bat 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin
            }
        }
        
        stage('Build') {
            steps {
                bat 'kubectl apply -f k8-multimule.yaml'                
            }
        }
        
    }
}
