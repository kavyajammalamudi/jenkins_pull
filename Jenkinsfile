pipeline {
    agent any

    stages {
        stage('Pull Ubuntu Image') {
            steps {
                script {
                    docker.image('ubuntu:latest').pull()
                }
            }
        }

        stage('Create Ubuntu Container') {
            steps {
                script {
                    docker.image('ubuntu:latest').withRun('-d -it --stop-timeout 300 -p 3306:3306') {
                        // Add your container-specific steps here, if any
                    }
                }
            }
        }
    }
