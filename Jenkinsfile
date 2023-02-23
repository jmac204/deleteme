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
        stage('Login and Push'){
            steps {
                script{
                    withDockerRegistry(credentialsId: 'Docker') {
                        docker.build('jeremymcintyre/vettec_flask_app').push('latest')
}
                }
            }
        }
 
        }
    }
}