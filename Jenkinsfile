pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                git branch: 'main', url: 'https://github.com/Saniajain1320/APD_jenkins_trial.git'
            }
        }

        stage('Build') {
            steps {
                sh './build.sh'
            }
        }

        stage('Test') {
            steps {
                sh './test.sh'
            }
        }

        stage('Quality Check') {
            steps {
                sh './quality.sh'
            }
        }

        stage('Deploy') {
            steps {
                sh './deploy.sh'
            }
        }
    }
}
