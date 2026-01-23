pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM',
                  branches: [[name: '*/main']],
                  doGenerateSubmoduleConfigurations: false,
                  extensions: [[$class: 'WipeWorkspace']],
                  userRemoteConfigs: [[url: 'https://github.com/sakshi0619/test.git']]
                ])
            }
        }

        stage('Compile Java') {
            steps {
                bat 'dir'              // Lists files in workspace (optional)
                bat 'javac hello.java' // Compile your Java file
                bat 'java hello'       // Run the program (optional)
            }
        }
    }
}


