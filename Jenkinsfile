pipeline {
    agent any

    environment {
        DOCKER = credentials('Docker')
    }

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t jeremymcintyre/vettec_flask_app .'
            }
        }
        stage('Login'){
            steps {
                echo '$DOCKER | docker login -u jeremymcintyre --password-stdin'
            }
        }
    }
}