pipeline {
    
    agent any
    
    environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerhub')
	}
    
    stages {
        
        stage('login'){
            steps {
                bat 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password dckr_pat_Z2BWXm4nITC8WJ-VbQBZ-qZ1IKc'
            }
        }
        
        stage('Build') {
            steps {
                bat 'kubectl apply -f k8-multimule.yaml'                
            }
        }
        
    }
}
