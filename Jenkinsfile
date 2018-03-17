#!/usr/bin/env groovy

pipeline {

    agent {
        docker {
            image 'centos'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'yum install tomcat -y'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'systemctl enable tomcat; systemctl start tomcat'
            }
        }
    }
}
