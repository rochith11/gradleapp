pipeline {
 agent any
 tools{
   gradle 'Gradle'
   jdk 'java17'
 }
 stages {
   stage ('Checkout') {
    steps {
      git branch:'master', url:'https://github.com/rochith11/gradleapp/blob/master/Jenkinsfile'
      }
     }
    stage ('Build') {
    steps {
      sh 'gradle build'
     }
    }
    stage ('Test') {
    steps {
    sh 'gradle test'
    }
    }
    
    stage ('Run Application'){ 
    steps {
    sh 'gradle run'
    }
    }
    }
    post {
    success {
    echo 'Build and Deploy successful'
    }
    failure {
    echo 'Build failed'
    }
   }
   }
