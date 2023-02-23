pipeline {
    agent any

    environment {
        DOCKER = credentials('Docker')
    }

    stages {
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
