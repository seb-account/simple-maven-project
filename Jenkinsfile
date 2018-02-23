pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                git url:'https://github.com/seb-account/simple-maven-project'
            }
        }

        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Deploy'){
            steps {
              sh 'cp target/simple-maven-webapp-1.0-SNAPSHOT.war /opt/tomcat/apache-tomcat-8.0.35/webapps'
            }
        }
    }

}
