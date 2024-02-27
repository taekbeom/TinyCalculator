pipeline {
    agent any
    
    stages {
        
        stage('Build') {
            steps {
                sh 'g++ -o TinyCalculator main.cpp'
            }
        }
        
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'TinyCalculator', fingerprint: true
            }
        }
    }
    
    post {
        success {
            echo 'Build successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
