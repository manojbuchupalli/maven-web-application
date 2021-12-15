node
{
    def mavenhome = tool name: "Maven 3.8.4"
    stage('CheckoutCode')
    {
        git branch: 'development', credentialsId: 'a16dfcae-ba31-4871-96ad-d52a8cbbe4bc', url: 'https://github.com/manojbuchupalli/maven-web-application.git'
    }
    
    stage('Build')
    {
        sh "${mavenhome}/bin/mvn clean package" 
    }
    /*
    stage('sonar')
    {
        sh "${mavenhome}/bin/mvn sonar:sonar"
    }
     stage('upload artifact to nexus')
    {
        sh "${mavenhome}/bin/mvn deploy"
    }
    stage('Deploy app to TomCat')
    {
        sshagent(['1fd6a76d-2b64-4811-a86d-4b7cc6643304']) 
        {
            sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.110.213.235:/opt/apache-tomcat-9.0.55/webapps/"
        }
    }
    stage ('email notification')
    {
        mail bcc: '', body: 'Completed', cc: ' ', from: '', replyTo: '', subject: 'Build', to: 'manojece4288@gmail.com'
    }
    */
}
