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
        stage('Welcome') {
            agent { label 'java_node' }
            steps {
                echo 'Welcome'
            }
        }
    }
}
