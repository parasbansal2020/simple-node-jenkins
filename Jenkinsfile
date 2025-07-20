pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/parasbansal2020/simple-node-jenkins.git'
                
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Build') {
            steps {
                sh 'zip -r build.zip .'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Build ....'
                sh 'mkdir -p deploy && cp build.zip deploy/'
                echo 'Deployed to ./deploy folder.'
            }
        }
    }
    
    
}
