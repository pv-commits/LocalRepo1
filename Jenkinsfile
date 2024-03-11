pipeline {
    agent any
    
    tools {
        // Define the Maven tool
        maven 'maven-3'
    }
    
    stages {
        stage('SCM checkout') {
            steps {
                git clone 'https://github.com/pv-commits/LocalRepo1'
            }
        }
        stage('Compile-Package') {
            steps {
                // Use the Maven tool
                sh "mvn package"
            }
        }
    }
}
