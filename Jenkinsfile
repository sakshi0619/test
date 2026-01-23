pipeline {
    agent any
    stages {
        stage('Run Java') {
            steps {
                bat 'javac Hello.java'
                bat 'java Hello'
            }
        }
        stage('Run Python') {
            steps {
                bat 'python hello.py'
            }
        }
    }
}

