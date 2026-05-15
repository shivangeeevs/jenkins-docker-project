
pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/shivangeeevs/jenkins-docker-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name mycontainer myapp'
            }
        }
    }
}


