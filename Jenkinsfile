pipeline {
   
    agent any

    stages{
        stage('Build'){
            steps{
                sh 'npm install'

            }
        }
        stage('test'){
            steps{
                sh 'echo "Test is running"'
            }
        }
        stage('deploy'){
            steps{
                sh 'echo "Deploying the application"'
            }
        }
    }




}