pipeline {
    
    agent any
    
    environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerhub')
	}
    
    stages {
        
        /*stage('login'){
            steps {
                bat 'echo "MT9Ai1H97" | docker login -u mathi610 --password-stdin'
            }
        }*/
        
        stage('Build') {
            steps {
		    bat 'docker run -d -p8081:8081 -p8082:8082 --name clust mathi610/cluster'                
            }
        }
        
    }
}
