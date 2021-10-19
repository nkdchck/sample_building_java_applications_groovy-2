@Library('jenkins-shared-lib') _

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                checkout scm
                sh 'chmod +x gradlew'
                sh './gradlew build'
            }
        }
        stage('Shared Library Test') {
            steps {
                welcome("Morty Smith")
                script {
                    calculator.add(3, 3)
                    calculator.mul(3, 5)
                } 
            } 
        }
    }
}
