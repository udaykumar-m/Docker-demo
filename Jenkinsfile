pipeline {
    agent any

    stages {

        stage("build") {
            steps {
                echo 'build app after 2 minutes pr'
            }
        }

        stage("test") {
            steps {
                echo 'test app'
            }
        }

        stage("deploy") {
            steps {
                echo 'deploy app'
            }
        }
    }
}