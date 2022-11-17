pipeline {
    agent any

    stages {
        stage('Clean Workspace'){
            steps{
                cleanWs()
            }
        }
        
        stage('Clone') {
            steps {
                git "https://github.com/PinkNapkin/simple-webapp-nodejs.git"
            }
        }
        
        stage('Build'){
            steps{
                nodejs('nodejs16') {
                    sh "npm install"
                }
            }
        }
        
        stage('Test'){
            steps
            {
                nodejs('nodejs16') {
                    sh "npm test"
                }
            }
            
        }
    }
}
