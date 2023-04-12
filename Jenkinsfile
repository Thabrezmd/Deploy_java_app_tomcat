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
                sh 'curl -T target/myapp.war "http://thabrez:Tabrez@99@13.234.113.97:8080/manager/text/deploy?path=/myapp&update=true"'
            }
        }
    }
}
