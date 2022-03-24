pipeline
{
    agent none
    
    environment {
        DEPLOY_TO="PRODUCTION"        
    }
    
    parameters {
        string(name: 'STAGE_NAME', defaultValue: '', description: 'Where should be install the value?')
        choice(name: 'CHOICE', choices: ['defect fix', 'testing', 'production'], description: 'what stage are you performing')
    }
  
    stages
    {
        stage('ContinuousDownload')
        {
            agent { label 'main' }
            
            when {
                beforeAgent true
                branch 'master'
                allOf {
                    expression {
                        return params.CHOICE == 'testing' && params.STAGE_NAME == 'TESTING'   
                    }
                    environment name:'DEPLOY_TO', value: 'PRODUCTION'
                }

            }
            
            steps
            {
                echo "Branch name: ${BRANCH_NAME}"
                echo "Tag name: ${env.TAG_NAME}"
                echo "Change Author: ${env.CHANGE_AUTHOR}"
                echo "STAGE_NAME: ${params.STAGE_NAME}"
                echo "CHOICE: ${params.CHOICE}"
                echo "DEPLOY_TO: ${env.DEPLOY_TO}"
            }
        }
    }    
}
