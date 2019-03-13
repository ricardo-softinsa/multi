pipeline{
    agent any
    stages{
        stage('First Dev'){
            steps{
                echo "${env.GIT_BRANCH}"
                script{                
                    if (env.BRANCH_NAME == "dev") {                                          
                        echo "First Dev"
                    }   
                }
            }
        }
        stage('First Prod'){
            steps{
                script{                
                    if (env.BRANCH_NAME == "master") {                                          
                        echo "First Prod"
                    }   
                }
            }
        }
        stage('Second Dev'){
            steps{
                script{                
                    if (env.BRANCH_NAME == "dev") {                                          
                        echo "First Dev"
                    }   
                }
            }
        }
        stage('Second Prod'){
            steps{
                script{                
                    if (env.BRANCH_NAME == "master") {                                          
                        echo "First Prod"
                    }   
                }
            }
        }
    }
}