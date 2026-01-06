pipeline {
    // agent { label 'java_node' }
    // agent { label 'slave1' }
    agent none
    stages {
        stage('Checkout') {
            agent { label 'java_node' }
            steps {
                echo 'Checking out the code'
                sh 'rm -rf *'
                sh 'git clone https://github.com/gsgeetha/hello-world-war.git'
            }
        }
        // stage('Build') {
        //     steps {
        //         echo 'Building the code'
        //         sh '''
        //             cd hello-world-war
        //             mvn clean package
        //         '''
        //        // sh 'mvn -f "hello-world-war/" clean package'
        //     }
        // }
        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying to tomcat'
        //         sh '''
        //             scp */target/*.war jenkins@172.31.9.48:/tmp
        //             ssh jenkins@172.31.9.48 "
        //                 sudo mv /tmp/*.war /opt/tomcat/webapps/
        //                 sudo /opt/tomcat/bin/startup.sh
        //             "
        //         '''
        //     }
        // }
    }
}
