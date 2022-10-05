pipeline {
    
    agent any
    
    environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerhub')
	}
    
    stages {
        
        stage('login'){
            steps {
                bat 'docker login -u $DOCKERHUB_CREDENTIALS_USR --password $DOCKERHUB_CREDENTIALS_PSW'
            }
        }
        
        stage('Build') {
            steps {
                bat 'kubectl apply -f k8-multimule.yaml'                
            }
        }
        
    }
}
