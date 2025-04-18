pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/RepositGit-cpu/DockerJenkinsExperiment'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t dockerjenkinsexperiment .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8081:80 dockerjenkinsexperiment'
            }
        }
    }
}
