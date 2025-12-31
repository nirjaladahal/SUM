pipeline {
    agent any

    stages {

        stage('Checkout source code') {
            steps {
                checkout scm
            }
        }

        stage('Install dependencies') {
            steps {
                bat '"C:\\Users\\PC\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Run single test') {
            steps {
                bat '"C:\\Users\\PC\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" test\\sum_of_two_numbers.py'
            }
        }

        stage('Run integration tests') {
            steps {
                bat '"C:\\Users\\PC\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" test\\integration_test.py'
            }
        }
    }
}
