pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'kubectl apply -f test2.yaml'                
            }
        }
    }
}
