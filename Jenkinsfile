node {
    stage('SCM Checkout'){
        git 'https://github.com/duartecardao/my-app' 
    }
    stage('Compile Package'){
        //Get maven homepath
        def mvnHome = tool name: 'maven-3', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Email Notification'){
        mail bcc: '', body: 'Jenkins jobs executed correctly.', cc: '', from: '', replyTo: '', subject: 'Pipeline executado correctamente', to: 'duarte.cardao@gmail.com'
    }
    stage('Slack Notification'){
        slackSend baseUrl: 'https://hooks.slack.com/services/',
         channel: '#general',
         color: 'good',
         message: 'Welcome to Jenkins slack!',
         tokenCredentialId: 'slack-demo',
         username: 'SlackNotification'
    }
}