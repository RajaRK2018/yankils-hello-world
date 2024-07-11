pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                echo 'Hello world!!'
                sh '''
                    sudo su -
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
    }
}