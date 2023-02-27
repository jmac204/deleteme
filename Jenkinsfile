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
        stage('AWS Commands'){
            steps {
                script {
                    withAWS(credentials: 'AWS_Credentials', region: 'us-east-1'){
                        sh 'aws sts get-caller-identity'
                    }
                }
            }
        }
 
    }
}
