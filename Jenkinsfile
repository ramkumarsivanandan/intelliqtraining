pipeline
{
    agent { label 'main' }
  
    stages
    {
        stage('ContinuousDownload')
        {
            steps
            {
                echo "Branch name: ${BRANCH_NAME}"
                echo "Tag name: ${env.TAG_NAME}"
                echo "Change Author: ${CHANGE_AUTHOR}"
            }
        }
    }    
}
