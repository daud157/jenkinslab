pipeline {
   
    agent any
  environment{
     DOCKERHUB_CREDENTIALS=credentials('dockerhub-6593')
  }
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
        stage('Docker build'){
            steps{
                sh 'sudo docker build -t daud611/jenkins-integration:latest .'
            }
        }
        stage('login'){
            steps{
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
            }
        }
        stage('push'){
            steps{
                sh 'sudo docker push daud611/jenkins-integration:latest'
            }
        }
        stage('deploy'){
            steps{
                sh 'echo "Deploying the application"'
            }
        }
      
    }




}