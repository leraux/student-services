#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'node'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn clean install package jar'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'maven clean test'
            }
        }
    }
}