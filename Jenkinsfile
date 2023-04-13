pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Deploy to Tomcat') {
            steps {
                sh 'curl -T target/01-maven-web-app.war "http://thabrez:Tabrez@99@13.235.17.92:8080/manager/text/deploy?path=/maven&update=true"'
            }
        }
    }
}
