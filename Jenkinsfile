pipeline {
    agent any

    stages {
        stage('Build Stage') {
            stages {
                stage('Inner Build Stage') {
                     steps {
                        echo 'Building..'
                        echo 'Building..'
                        echo 'Building..'
                        echo 'Building..'
                        echo 'Building..'
                     }
                }
            }
        }
        stage('Test Stage') {
            steps {
                echo 'Testing..'
                echo 'Testing..'
                echo 'Testing..'
                echo 'Testing..'
                echo 'Testing..'
            }
        }
        stage('Deploy Stage') {
            steps {
                echo 'Deploying....'
                echo 'Deploying....'
                echo 'Deploying....'
                echo 'Deploying....'
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