//CODE_CHANGES = getGitChanges()
pipeline {
    agent any
    
    // Environmets stated here are available to all stages
    environment {
        NEW_VERSION = "1.3.0"
    }
    stages {
        stage("build"){
            steps{
                echo "Hello Build"
                echo "Building Version ${NEW_VERSION}"
            }
        }
        stage("test"){
            when {
                expression {
                    BRANCH_NAME == 'dev' || BRANCH_NAME == "main"
                }
            }
            steps{
                echo "Hello test"
            }
        }

        stage("deploy"){
            steps{
                echo "Hello test"
            }                        
        }
    }
}


node {
    // groovy script
}