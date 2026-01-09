pipeline
{
    agent any
    stages
    {
      stage('Download')
     {
       steps
       {
         git 'https://github.com/IntelliqDevops/maven.git'
       }
     }
     stage('Build1')
     {
      steps
       {
        sh 'mvn package'
       }
      }
      stage('Deploy')
      {
       steps
       {
        sh "scp /var/lib/jenkins/workspace/MultiBranchPipeline/webapp/target/webapp.war ubuntu@172.31.27.73:/var/lib/tomcat10/webapps/testapp.jar"
       }
      }
   }
}
