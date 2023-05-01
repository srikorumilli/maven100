@Library("mylibrary")_
node('built-in')
{
    stage('continusDownload-master')
    {
        cicd.newGit("maven")
    }
    stage('continuesBuild-master')
    {
        cicd.newMaven()
    }
    
    
}

