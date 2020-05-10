#!groovy
pipeline {
    options {
        timeout(time: 1, unit: 'HOURS')
    }
    agent any
    stages {
        stage('clean') {
            steps {
                sh 'npm cache clean --force'
            }
        }
        stage('init') {
            steps {
                sh 'npm install'
            }
        }
        stage('build') {
            steps {
                sh 'npm run build'
            }
        }
    }
    post {
        success {
            script {
                if (env.BRANCH_NAME != 'master') {
                   // latestTag = sh(returnStdout: true, script: "git describe --tags --abbrev=0").trim()
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                        def customImage = docker.build("saja/udacity-c3-frontend:0.0.0")
                        customImage.push()
                    }
                }
            }
        }
    }
}
