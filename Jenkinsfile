pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                git url: "git@github.com:Shaheen8954/simple-nodejs-people-info-app.git"
            }
        }
        stage('docker build') {
            steps {
                sh "docker build -t simple-node ."
            }
        }
        stage('docker run') {
            steps {
                sh "docker run -d -p 3000:3000 simple-node"
            }
        }
    }
}
