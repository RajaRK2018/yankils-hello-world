pipeline {
    agent any 
    tools {
        maven 'maven-3.9.8'
        jdk 'java-11'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Deploying Webapp on Tomcat'
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                    mvn -v
                    mvn clean install
                    mvn tomcat7:deploy
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