pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               //bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/princy1612/demo_test.git"
                bat "npm clean  demo_test"
            }
        }
        stage('install') {
            steps {
                bat "npm install demo_test"
            }
        }
        stage('test') {
            steps {
                bat "npm test  demo_test"
            }
        }
        stage('package') {
            steps {
                bat "npm package  demo_test"
            }
        }
    }
}
