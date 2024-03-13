node {
    stage('SCM Checkout') {
        git branch: 'main', url: 'https://github.com/pv-commits/LocalRepo1.git'
    }
    stage('Compile-Package') {
        // Get maven home path
        def mvnHome = tool 'maven-3'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Email Notification') {
      mail bcc: '', body: '''Hi Team,
      Welcome to jenkins email alerts
      Thanks,
      Puru''', cc: '', from: '', replyTo: '', subject: 'Jenkins Jobs', to: 'pbaghe03@gmail.com'
    }
    stage('slack notification') {
        slackSend baseUrl: 'https://hooks.slack.com/services/', 
        channel: '#jenkins-pipeline-demo', 
        color: 'good', 
        message: 'Welcome to jenkins, slack!', 
        tokenCredentialId: 'slack-demo', 
        username: 'javahomecloud'
    }
}
