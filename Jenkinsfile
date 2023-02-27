pipeline {
    agent any

    stages {
        stage('Login Build and Push'){
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
