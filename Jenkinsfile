pipeline {
    agent any 
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