pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Shivammdh/dockerdjango.git']]])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/Shivammdh/dockerdjango.git'
                
            }
        }
        stage('Test') {
            steps {
                sh 'python3 manage.py runserver'
            }
        }
    }
}
