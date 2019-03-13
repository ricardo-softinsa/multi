pipeline{
    agent any
    stages{
        stage('First Dev'){
            steps{
                //echo bat(returnStdout: true, script: 'set')
                script{                
                    if (env.BRANCH_NAME == "origin/dev") {                                          
                        echo "First Dev"
                    }   
                }
            }
        }
        stage('First Prod'){
            steps{
                script{                
                    if (env.BRANCH_NAME == "origin/master") {                                          
                        echo "First Prod"
                    }   
                }
            }
        }
        stage('Second Dev'){
            steps{
                script{                
                    if (env.BRANCH_NAME == "origin/dev") {                                          
                        echo "First Dev"
                    }   
                }
            }
        }
        stage('Second Prod'){
            steps{
                script{                
                    if (env.BRANCH_NAME == "origin/master") {                                          
                        echo "First Prod"
                    }   
                }
            }
        }
    }
}