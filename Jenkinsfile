pipeline {
    agent any

    Parameters{
        choice(name:'VERSION', choices:['1.1.0','1.2.0','1.3.0'])
    }

    stages {

        stage("build") {
            steps {
                echo 'build app after 2 minutes pr'
                nodejs('Node-10.17') {
                    sh 'yarn install'
                }
            }
        }

        stage("test") {
            when {
                expression{
                    Branch_NAME == 'jenkins'
                }
            }
            steps {
                echo 'test app'
            }
        }

        stage("deploy") {
            steps {
                echo "deploy app ${params.VERSION}"
            }
        }
    }
}