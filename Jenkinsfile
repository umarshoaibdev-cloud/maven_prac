pipeline
{
	agent any
	stages
	{
		stage("Download")
   		{
			steps
			{
				git "https://github.com/umarshoaibdev-cloud/maven_prac.git"
			}
		}
		stage("Build")
	 	{
			steps
		 	{
			 	sh 'mvn package'
			}
		}
		stage("Deploy")
		{
			steps
			{
				sh 'scp /var/lib/jenkins/workspace/DeclarativePipelineUsingScp/webapp/target/webapp.war ubuntu@172.31.27.73:/var/lib/tomcat10/webapps/testapp.jar'
			}
		}
		stage("Testing")
		{
			steps
			{
				git "https://github.com/IntelliqDevops/FunctionalTesting.git"
			}
		}
	}
}
