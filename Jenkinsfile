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
                // sh '''
                //     pwd
                //     ls
                //     cd hello-world-war
                //     pwd
                //     ls
                //     mvn clean package
                // '''
               sh 'mvn -f "hello-world-war/" clean package'
            }
        }
    }
}
