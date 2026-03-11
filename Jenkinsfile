pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                echo 'Pulling source code from Git repository...'
                git branch: 'main', url: 'https://github.com/Saniajain1320/APD_jenkins_trial.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Running Build Stage...'
                bat 'Build.bat'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Test Stage...'
                bat 'Test.bat'
            }
        }

        stage('Quality Check') {
            steps {
                echo 'Running Quality Gate...'
                bat 'Quality.bat'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Running Deploy Stage...'
                bat 'Deploy.bat'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
