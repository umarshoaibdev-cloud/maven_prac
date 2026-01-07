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
			 	sh 'mnv package'
			}
		}
	}
}
