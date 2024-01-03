pipeline{
    agent any
    stages{
        stage('code') {
            steps {
                git branch: 'main', url: 'https://github.com/shaiksulthanhussainvali/Project-3-Django-Application.git'
            }
        }
        stage("Build"){
            steps{
                sh "docker build . -t django-application"
            }
        }
        stage("Pushing to Docker Hub"){
            steps{
                withCredentials([usernamePassword(credentialsId:"Docker-Hub-Credentials",passwordVariable: 'Yaswanthk@789', usernameVariable: 'yaswanthk2059')]){
                sh "docker tag django-application ${env.yaswanthk2059}/django-application:latest"
                sh "docker login -u ${env.yaswanthk2059} -p ${env."Yaswanthk@789"}"
                sh "docker push ${env.yaswanthk2059}/django-application:latest"
                }
            }
        }
        stage("Deploy"){
            steps{
                echo "deploy"
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
