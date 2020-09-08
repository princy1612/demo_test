pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               //bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                bat "npm clean  TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                bat "npm install  TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                bat "npm test  TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                bat "npm package  TicketBookingServiceJunitTesting"
            }
        }
    }
}
