pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage('EnvVars'){
            steps {
               script {
                   def fields = env.getEnvironment()
                   fields.each {
                        key, value -> println("${key} = ${value}");
                    }

                    println(env.PATH)
               }
            }
        }

        stage ('Build') {
            steps {
                sh './mvnw clean package'
            }
            post {
                always {
                    junit 'target/surefire-reports/**/*.xml'
                }
            }
        }
    }
}