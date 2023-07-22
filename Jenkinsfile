@Library('jenkins-libs') _
pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                helloWorld()
            }
        }
        stage('clone') {
            steps {
                git branch: 'main', credentialsId: 'jenkinstest', url: 'https://github.com/karthiksaranam/jenkins.git'
            }
            
        }
        stage('build') {
            steps {
                sh 'docker build .'
            }
            sh "cd ${workspace}"
        }
    }
}