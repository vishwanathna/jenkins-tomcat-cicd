pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/vishwanathna/jenkins-tomcat-cicd.git'
            }
        }
        stage('Maven Compilation') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('Maven Testing') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Maven Packaging') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Tomcat Deployment') {
            steps {
                deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'tomcat-creds', path: '', url: 'http://54.164.19.22:8080/')], contextPath: 'moviehub', war: '**/*.war'
            }
        }
    }
}
