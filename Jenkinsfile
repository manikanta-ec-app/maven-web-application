node
{
   def mavenHome = tool name: "maven3.6.2"
   
    stage('CheckoutCode')
    {
        git branch: 'development', credentialsId: 'b072cfd8-f82f-4af0-993f-38520fc83eb7', url: 'https://github.com/manikanta-ec-app/maven-web-application.git'
    }
    stage('Build')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }

   /*
   stage('ExecuteSonarQube')
    {
        sh "${mavenHome}/bin/mvn sonar:sonar"
    }
    stage('ArtifactoryReposityNEXUS')
    {
        sh "${mavenHome}/bin/mvn clean deploy"
    }
    stage('DeployintoTomcat')
    {
        sshagent(['bb480a3c-e02c-4ce5-b818-55f38cf558e0']) 
        {
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.235.221.237:/opt/apache-tomcat-8.5.65/webapps/"
    
}
    }
    stage('SendEmailNotification')
    {
        mail bcc: '', body: '''Build over

Regards,
Manikanta G,
9441523409.''', cc: 'gummidipudim@gmail.com', from: '', replyTo: '', subject: 'Build ver', to: 'info.manig167@gmail.com'
    }
*/
}

