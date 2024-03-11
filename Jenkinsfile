node {
    stage('SCM Checkout') {
        steps {
            git branch: 'main', url: 'https://github.com/pv-commits/LocalRepo1.git'
        }
    }
    stage('Compile-Package') {
        // Get maven home path
        def mvnHome = tool 'maven-3'
        sh "${mvnHome}/bin/mvn package"
    }
}
