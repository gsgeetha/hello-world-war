pipeline {
    // agent { label 'java_node' }
    agent { label 'slave1' }
    // agent none
    // agent any 
    
    parameters {
        string(name: 'CMD', defaultValue: 'cd', description: 'Command used to run/build application')
        booleanParam(name: 'RUN_TESTS', defaultValue: false, description: 'Run tests?')
        choice(name: 'CMD1', choices: ['clean', 'validate', 'compile', 'verify', 'deploy'], description: 'Different Maven Commands')
    }
    stages {
        stage('Parallel stage') {
            parallel {
                stage('Stage 1') {
                    steps {
                        sh 'echo "Running Stage 1"'
                    }
                }

                stage('Stage 2') {
                    steps {
                        sh 'echo "Running Stage 2"'
                    }
                }
            }
        }
            
            // stage('Get the tomcat credentials') {
            //     steps {
            //     withCredentials([
            //                         usernamePassword(
            //                             credentialsId: 'tomcat',
            //                             usernameVariable: 'USERNAME',
            //                             passwordVariable: 'PASSWORD'
            //                         )
            //                     ]) {
            //         sh ' echo $USERNAME $PASSWORD'
            //         }
            //     }
            // }
            // stage('Get the git credentials') {
            //     steps {
            //     withCredentials([
            //                         git(
            //                             credentialsId: 'git_token',
            //                             usernameVariable: 'GIT_USERNAME',
            //                             passwordVariable: 'GIT_TOKEN'
            //                         )
            //                     ]) {
            //         sh ' echo $GIT_USERNAME $GIT_TOKEN'
            //         }
            //     }
            // }
    }
}
