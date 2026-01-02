node('built-in')
{
    stage('Download')
    {
        git 'https://github.com/umarshoaibdev-cloud/maven.git'
    }
    stage('Build')
    {
        sh 'mvn package'
    }
    stage('Deploy')
    {
        sh 'scp /var/lib/jenkins/workspace/MultiplePipelines/webapp/target/webapp.war ubuntu@172.31.7.54:/var/lib/tomcat10/webapps/testapp.war'
    }
    stage('Test')
    {
        git 'https://github.com/IntelliqDevops/FunctionalTesting.git'
        sh 'java -jar /var/lib/jenkins/workspace/MultiplePipelines/testing.jar'
    }
   stage('Delivery')
    {
        sh 'scp /var/lib/jenkins/workspace/MultiplePipelines/webapp/target/webapp.war ubuntu@172.31.14.227:/var/lib/tomcat10/webapps/prodapp.war'
    }
}
