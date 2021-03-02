node

{
def mavenHome=tool name: "maven3.6.3"

stage ("getcode")
{
git branch: 'development', credentialsId: 'eed3d75e-3ba4-4b0b-a1ea-6884713fa08f', 
url: 'https://github.com/parunayak/maven-web-application.git'
}

stage ("build")
{

sh "${mavenHome}/bin/mvn clean package"
}
   
/*   
stage ("SonarQubereport")
{

sh "${mavenHome}/bin/mvn sonar:sonar"

}

stage ("Artifactoryrepo")
{

sh "${mavenHome}/bin/mvn deploy"

}

stage ("Deployappintotomcat")
{

sshagent(['4e49752f-fc1b-41ff-b02f-7a1d8a29d3d6']) 
{
   sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@52.66.19.34:/opt/apache-tomcat-9.0.43/webapps/"
}

}
stage ("SendEailNotification")
{
emailext body: '''Build Over!..

Regards,
Islavath Parvathi,''', subject: 'Build Over', to: 'iparvathi229@gmail.com'

}
*/
}
