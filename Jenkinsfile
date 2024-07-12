pipeline {
    agent any 
    tools {
        maven 'Maven 3.9.8'
        jdk 'jdk11'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Hello world!!'
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
    }
}