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
    stage('continusDeployement-master')
    {
        cicd.newDeploy("ScriptedPipelinewithSharedLibraries","172.31.26.176","testapp")
    
    }
    stage('continousTesting-master')
    {
        cicd.newGit("FunctionalTesting")
        cicd.executeSelenium("ScriptedPipelinewithSharedLibraries")
    }
    stage('continuosDelivery-master')
    {
       cicd.newDeploy("ScriptedPipelinewithSharedLibraries","172.31.26.162","prodapp") 
    }
    
}

