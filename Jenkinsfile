pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh 'docker build -t jeremymcintyre/vettec_flask_app .'
            }
        }
    }
}