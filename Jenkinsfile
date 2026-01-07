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
				sh 'scp /var/lib/jenkins/workspace/DeclarativePipelineUsingScp/webapp/target/webapp.war ubuntu@172.31.27.73:/var/lib/tomat10/webapps/testapp.jar'
			}
		}
	}
}
