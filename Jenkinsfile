node {
  stage('SCM Checkout') {
        git 'https://github.com/jkjit/hellowebworld.git'
        }
   stage('Compile Project'){
     //Get MAVEN HOME PATH
     def mvnHome = tool name: 'mymvn3', type: 'maven'
     sh "${mvnHome}/bin/mvn clean package"
       }
  stage('Docker build'){
    //Building docker image from git
    sh "docker build -t hellowebworld ."
  }
  
  stage('Email Notification'){
//  mail bcc: '', body: '''Hi WELCOME TO JENKINS EMAIL ALERT
//Thanks JayaKumar''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'jkck99@gmail.com'
    echo 'Successfully sent dummy email JK'
  }  

}
