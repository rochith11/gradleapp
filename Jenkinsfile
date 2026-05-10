pipeline {
 agent any
 tools{
   gradle 'Gradle'
   jdk 'jdk17'
 }
 stages {
   stage ('Checkout') {
    steps {
      git branch:'master', url:''
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
