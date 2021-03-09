node
{
def mavenHome = tool name: 'maven3.6.3'
stage('1.Codeclone')
git credentialsId: 'github_credentials', url: 'https://github.com/tomiosikoya/maven-web-app.git'
stage('2.maven-Build')
{ 
sh "${mavenHome}/bin/mvn package"
}
stage('3.CodeQualityReport')
{
//sh "${mavenHome}/bin/mvn sonar:sonar"
}
stage('4.UploadNexus')
{
//sh "${mavenHome}/bin/mvn deploy"
}
stage('5.Approval')
{
echo "Approved. Ready for deployment"
}
stage('6.DeployTomcat')
{
//deploy adapters: [tomcat9(credentialsId: 'Tomcat_creds', path: '', url: 'http://3.15.196.8:8888/')], contextPath: null, war: 'target/*war'
}   
stage('7.Notification')
{
//emailextrecipients([developers()])
} 
} 

//
/*
the
this
they
*/
