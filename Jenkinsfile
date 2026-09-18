pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn -B clean install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'mvn test'
            }
        }
        stage('Deploy to Test Environment') {
            steps {
                echo 'Deploying to Test...'
                // Test deployment commands would go here
            }
        }
        stage('Production Approval') {
            steps {
                input message: 'Tests passed and deployed to Test. Approve deployment to Production?'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                // Production deployment commands would go here
            }
        }
    }
}
