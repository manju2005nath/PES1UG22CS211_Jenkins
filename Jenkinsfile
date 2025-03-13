pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'g++ -o main/hello_exec main/hello.cpp'
                build 'PES1UG22CS211-1'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'cd main && ./hello_exec'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh '''
                    echo "Deployment would happen here in a real environment"
                    echo "Application successfully deployed!"
                '''
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
