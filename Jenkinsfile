node{
  stage('SCM checkout'){
    git 'https://github.com/pv-commits/LocalRepo1'
  }
  stage('Compile-Package'){
    //Get maven home path
    def mvnHome = tool name: 'maven-3', type: 'maven'
    sh "${mvnHome}/bin/mvn package"
  }
}
