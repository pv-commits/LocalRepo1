node{
    stage('SCM Checkout'){
        git 'https://github.com/pv-commits/LocalRepo1'
    }
    stage('Compile-Package'){
        sh 'mvn package'
    }
}
