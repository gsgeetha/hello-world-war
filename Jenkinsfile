@Library('shared_library@main') _  // Correct syntax

pipeline {
    agent { label 'slave1' }
    stages {
        stage('Checkout Code') {
            steps {
                script {
                     pipelinecode.checkoutcode()
                }
            }
        }
        stage('Setup Maven') {
            steps {
                setupmaven()
            }
        }
        stage('Build App') {
            steps {
                buildapp('package')
            }
        }
    }
}
