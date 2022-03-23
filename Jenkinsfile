pipeline
{
    agent { label 'linuxslave' }
  
    stages
    {
        stage('ContinuousDownload')
        {
            steps
            {
                echo "Branch name: ${BRANCH_NAME}"
                echo "Tag name: ${TAG_NAME}"
                echo "Change Author: ${CHANGE_AUTHOR}"
            }
        }
    }    
}
