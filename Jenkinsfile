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
                sh '''
                    cd hello-world-war
                    mvn clean package
                '''
               // sh 'mvn -f "hello-world-war/" clean package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to tomcat'
                sh 'scp */target/*.war ubuntu@172.31.9.48:/opt/apache-tomcat-10.1.50/webapps/'
            }
        }
    }
}
