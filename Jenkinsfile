pipeline {
    agent none
    stages {
        stage('Initialize') {
            agent any
            steps {
                sh('printenv | sort')
            }
        }
        stage('Test Stage 1') {
            agent {
                label('worker')
            }

            steps {
                sh './mvnw clean package'
            }
        }
        stage('Test Stage 2') {
            agent {
                label('worker')
            }

            steps {
                sh './mvnw clean package'
            }
        }
        stage('Test Stage 3'){
            agent {
                label('worker')
            }

            steps {
                sh './mvnw clean package'
            }
        }
    }
}