pipeline {
    agent any

    stages {
        stage('Build') {
            steps {                
                build 'PES2UG21CS450-1'
                sh 'g++ task5.cpp -o output'                
            }
        }
        stage('Test') {
            steps {                
                sh './output'                
            }
        }
        stage('Deploy') {
            steps {                
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
