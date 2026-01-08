@Library('shared_library@main') _  // Correct syntax

pipeline {
    agent { label 'slave1' }


    stages {
        stage('Checkout Code') {
            steps {
                checkoutcode()
            }
        }
    }
}
