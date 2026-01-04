pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code'
                sh 'rm -rf *'
                sh 'git clone https://github.com/gsgeetha/hello-world-war.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the code'
                sh 'ls'
                sh 'cd hello-world-war'
                sh 'ls'
                sh 'mvn clean package'
            }
        }
    }
}
