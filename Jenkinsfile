pipeline {
    agent any

    stages {
        stage('cloning the repository') {
            steps {
                git 'https://github.com/Monishs12345/Dockerized-Static-Web-Application.git'
            }
        }
        stage('building image') {
            steps {
                 bat '''docker build -t health_project .
                     '''
            }
        }
        stage('creating the container') {
            steps {
                 bat 'docker run -d -p 8085:80 --name container health_project'
            }
        }
        stage('pushing image to dockerhub') {
            steps {
                 bat ''' docker login -u monish03 -p Monish@2003
                 docker tag health_project monish03/health_project:v1
                 docker push monish03/health_project:v1
                     '''
            }
        }
    }
}
