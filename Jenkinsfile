pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'kubectl apply -f k8-multimule.yaml'                
            }
        }
    }
}
