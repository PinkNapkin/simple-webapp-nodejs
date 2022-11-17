pipeline {
    agent any
    stages {
        stage("Initialize") {
            steps {
                cleanWs()
            }
        }
        stage('Get SCM') {
            steps {
                git "https://github.com/PinkNapkin/simple-webapp-nodejs.git"
            }
        }
        stage('Build') {
            steps {
                sh "docker build -t nodewebapp ."
                sh "docker images"
            }
        }
    }
}
