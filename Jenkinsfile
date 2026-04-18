pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'echo "build step"'
            }
        }

        stage('SonarQube Analysis') {
            environment {
                SONAR_TOKEN = credentials('sonar-token')
            }
            steps {
                sh '''
                mvn clean verify sonar:sonar \
                -Dsonar.projectKey=tpjenkins \
                -Dsonar.host.url=http://sonarqube:9001 \
                -Dsonar.login=$SONAR_TOKEN
                '''
            }
        }
    }
}
