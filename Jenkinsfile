pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
        stage('Deploy'){
            steps {
              sh 'cp target/simple-maven-webapp-1.0-SNAPSHOT.war opt/tomcat/apache-tomcat-8.0.35/webapps'
            }
        }
    }

}
