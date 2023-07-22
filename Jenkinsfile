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
            git branch: 'main', credentialsId: 'jenkinstest', url: 'https://github.com/karthiksaranam/jenkins.git'
        }
        stage('build') {
            echo 'testing docker'
        }
    }
}