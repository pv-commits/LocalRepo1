node {
    stage('SCM Checkout') {
        git 'https://github.com/pv-commits/LocalRepo1'
    }
    stage('Compile-Package') {
        // Get maven home path
        def mvnHome = tool 'maven-3'
        sh "${mvnHome}/bin/mvn package"
    }
}
