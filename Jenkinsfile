
node
{
    def mavenHome = tool name: "maven3.8.5"
    
    stage('CheckOut')
    {
        git branch: 'development', credentialsId: '50dcf04b-9db7-418f-b982-24037693d33f', url: 'https://github.com/vickyc777/maven-web-application.git'
    }
    
    stage('Build')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    
    /*
    stage('ExecuteSonarQubeReport')
    {
        sh "${mavenHome}/bin/mvn sonar:sonar"
    }
    
     stage('UploadArtifactIntoNexus')
    {
        sh "${mavenHome}/bin/mvn deploy"
    }
    
    stage('DeployAppIntoTomcatServer')
    {
        sshagent(['342ec2b7-453c-4872-8943-a125427ee423']) {
        sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@13.126.252.218:/opt/apache-tomcat-9.0.62/webapps"
}
    }
    
    stage('SendEmailNotification')
    {
        mail bcc: 'vickyarthur7@gmail.com', body: '''Build finished..

       Regards,
       Vicky''', cc: 'vickyarthur7@gmail.com', from: '', replyTo: '', subject: 'Build finished..', to: 'vickyarthur7@gmail.com'
 }
 */
}
