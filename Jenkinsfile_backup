pipeline {
    // agent { label 'java_node' }
    // agent { label 'slave1' }
    // agent none
    agent any 
    
    parameters {
        string(name: 'CMD', defaultValue: '', description: 'Command used to run/build application')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run tests?')
        choice(name: 'CMD1', choices: ['clean', 'validate', 'compile', 'verify', 'deploy'], description: 'Different Maven Commands')
    }
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
