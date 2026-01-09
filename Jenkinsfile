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
        stage('Build')
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
        stage('Testing')
        {
            steps
            {
                git 'https://github.com/IntelliqDevops/FunctionalTesting.git'
                sh 'java -jar /var/lib/jenkins/workspace/MultiBranchPipeline/testing.jar'
            }
        }
	stage('Delivery)
	{
	   steps
	   {
		 sh "scp /var/lib/jenkins/workspace/MultiBranchPipeline/webapp/target/webapp.war ubuntu@172.31.24.59:/var/lib/tomcat10/webapps/prodapp.jar"	
	   }
	}
   }
}
