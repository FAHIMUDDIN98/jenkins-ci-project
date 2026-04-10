pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/FAHIMUDDIN98/jenkins-ci-project'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Test Report') {
            steps {
                junit 'target/surefire-reports/*.xml'
            }
        }
    }
}
