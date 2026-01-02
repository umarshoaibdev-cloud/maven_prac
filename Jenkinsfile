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
}
