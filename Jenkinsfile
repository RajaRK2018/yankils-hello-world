pipeline {
    agent any 
    tools {
        maven 'maven-3.9.8'
        jdk 'java-11'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Hello world!!!'
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                    mvn -v
                    mvn clean install
                '''
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: 'webapp/target/*', fingerprint: true
        }
    }
}