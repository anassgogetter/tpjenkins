pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/anassgogetter/tpjenkins'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "build working"'
            }
        }
    }
}
