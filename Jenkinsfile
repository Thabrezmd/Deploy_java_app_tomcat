pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

       // stage('Deploy to Tomcat') {
         //   steps {
        //        sh 'curl -T target/01-maven-web-app.war "http://thabrez:Tabrez@99@13.235.17.92:8080/manager/text/deploy?path=/maven&update=true"'
      //      }
    //    }
    stage('Stage-9 : Deployment - Deploy a Artifact devops-3.0.0-SNAPSHOT.war file to Tomcat Server') { 
            steps {
                sh 'curl -u thabrez:Tabrez@99 -T target/01-maven-web-app.war "http://13.235.17.92:8080/manager/text/deploy?path=/maven&update=true"'
            }
        } 
  
          stage('Stage-10 : SmokeTest') { 
            steps {
                sh 'curl --retry-delay 10 --retry 5 "http://13.235.17.92:8080/maven"'
            }
        }
    }
}
