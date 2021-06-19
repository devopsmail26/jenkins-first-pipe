node{
    def name = "DUDE"
    echo "welcome ${name} to AJHUB"
    stage('SCM checkout'){
        
        git 'https://github.com/devopsmail26/jenkins-first-pipe.git'
    }
    stage('Compile Package'){
        
        def mvnHome = tool name: 'maven-1', type: 'maven'
        
        sh "${mvnHome}/bin/mvn package"
    }
    stage('email sending'){
        mail bcc: '', body: '''HI dude,

        We are testing the jenkins job with mail.

        Regards,
        Jingidi''', cc: '', from: '', replyTo: '', subject: 'Jenkins test job', to: 'anveshj33@gmail.com'   
    }
    stage('slack notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/', 
       channel: 'software-jingidies', 
       color: 'good', message: 'testing pipelines scripts with jingidies', 
       teamDomain: 'anveshj33', 
       tokenCredentialId: 'software-jingidies-slack-token', 
       username: 'Jenkins jingidy'
    }
}
