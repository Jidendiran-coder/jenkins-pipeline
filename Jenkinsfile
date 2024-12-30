pipeline {
  agent any
  tools { maven "Maven" }
  stages {
    stage("Clone") {
      steps {
        git url: "https://github.com/<your-username>/spring-boot-app.git"
      }
    }
    stage("Build") {
      steps {
        sh "mvn clean install"
      }
    }
    stage("Run") {
      steps {
        sh "java -jar target/myapp-1.0-SNAPSHOT.jar"
      }
    }
  }
}
