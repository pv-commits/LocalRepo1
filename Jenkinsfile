pipeline {
  agent any
  
  stages {
    stage('SCM checkout') {
      steps {
        git 'https://github.com/pv-commits/LocalRepo1'
      }
    }
    stage('Compile-Package') {
      steps {
        // Get Maven home path
        def mvnHome = tool 'maven-3'
        sh "${mvnHome}/bin/mvn package"
      }
    }
  }
}
