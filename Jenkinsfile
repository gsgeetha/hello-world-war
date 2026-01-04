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
                sh 'pwd'
                sh 'find . -type f -iname "pom.xml"'
                sh 'mvn clean package'
            }
        }
    }
}
