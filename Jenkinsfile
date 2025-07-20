pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/parasbansal2020/paras-calculator/tree/ae33d283e159142bb7561131ed722dd8006eedd9/Day-1'
                
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
