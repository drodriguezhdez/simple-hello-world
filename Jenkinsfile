pipeline {
    agent any
    stages {
        stage('BuildAndTest') {
            matrix {
                    axes {
                        axis {
                            name 'PLATFORM'
                            values 'linux', 'mac', 'windows'
                        }
                        axis {
                            name 'BROWSER'
                            values 'chrome', 'edge', 'firefox', 'safari'
                        }
                    }
                    stages {
                            stage('Non-Parallel Stage') {
                                steps {
                                    echo 'This stage will be executed first.'
                                }
                            }
                            stage('Parallel Stage') {
                                when {
                                    branch 'master'
                                }
                                stages {
                                    stage('Branch A') {
                                        agent any
                                        steps {
                                            echo "On Branch A"
                                        }
                                    }
                                    stage('Branch B') {
                                        agent any
                                        steps {
                                            echo "On Branch B"
                                        }
                                    }
                                    stage('Branch C') {
                                        agent any
                                        stages {
                                            stage('Nested 1') {
                                                steps {
                                                    echo "In stage Nested 1 within Branch C"
                                                }
                                            }
                                            stage('Nested 2') {
                                                steps {
                                                    echo "In stage Nested 2 within Branch C"
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        }
                }
        }
    }

}