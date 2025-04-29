pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                git url: "https://github.com/Shaheen8954/simple-nodejs-people-info-app.git", branch: "main"
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
