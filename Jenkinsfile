pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               //bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                bat "npm clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                bat "npm install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
                bat "npm test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                bat "npm package -f TicketBookingServiceJunitTesting"
            }
        }
    }
