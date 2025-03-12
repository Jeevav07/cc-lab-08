pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o pes2ug23cs812 main/hello.cpp'
                echo 'Build stage completed successfully'
            }
        }
        
        stage('Test') {
            steps {
                sh './pes2ug23cs812’
                echo 'Test stage completed successfully'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment stage completed successfully'
                echo 'Deployed the application'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline executed successfully'
        }
    }
}
