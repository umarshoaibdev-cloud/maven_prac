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
}
