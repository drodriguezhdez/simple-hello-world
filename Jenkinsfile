pipeline {
    agent any

    stages {
        stage('Build') {
            echo 'Building..'
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo 'I will always say Hello again!'
        }
    }
}