node {
   stage('SCM Checkout') {
 
       git 'https://github.com/bierbios/maven1.git'
       
   }
   
   stage('compile-package'){
       def home_maven = tool name: 'maven1', type: 'maven'
      sh "${home_maven}/bin/mvn package"
   }
   
   stage('Slack Notification'){
        slackSend baseUrl: 'https://hooks.slack.com/services/', 
         channel: '#testing', 
         color: 'good', 
         message: 'Selamat Datang', 
         tokenCredentialId: 'slack-demo', 
         username: 'erbiantonug@gmail.com'
   }
   
   
}
