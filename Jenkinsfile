pipeline {
    agent any
    
    stages {
        
        stage('Build') {
            steps {
                sh 'g++ -o TinyCalculator.exe main.cpp'
            }
        }
        
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'TinyCalculator.exe', fingerprint: true
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
