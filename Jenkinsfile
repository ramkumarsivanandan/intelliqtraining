pipeline
{
    agent none
    
    parameters {
        string(name: 'STAGE_NAME', defaultValue: '', description: 'Where should be install the value?')
        choice(name: 'CHOICE', choices: ['defect fix', 'testing', 'production'], description: 'what stage are you performing')
    }
  
    stages
    {
        stage('ContinuousDownload')
        {
            agent { label 'main' }
            
            steps
            {
                echo "Branch name: ${BRANCH_NAME}"
                echo "Tag name: ${env.TAG_NAME}"
                echo "Change Author: ${env.CHANGE_AUTHOR}"
                echo "STAGE_NAME: ${params.STAGE_NAME}"
                echo "CHOICE: ${params.CHOICE}"
            }
        }
    }    
}
