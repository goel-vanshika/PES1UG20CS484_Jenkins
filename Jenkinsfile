pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ Pipeline_484.cpp -o Pipeline_484'
                sh 'jenkins-cli.jar -s http://localhost:8080/ build PES1UG20CS484-1'
            }
        }
        stage('Test') {
            steps {
                sh './Pipeline_484'
            }
        }
        stage('Deploy') {
            steps {
                echo "Deployement Successfull"
            }
        }
    }
    
    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
