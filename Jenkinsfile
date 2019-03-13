pipeline{
    agent any
    stages{
        stage('First Dev'){
            steps{
                //echo bat(returnStdout: true, script: 'set')
                echo "${env.GIT_BRANCH}"
                script{                
                    if (env.GIT_BRANCH == "origin/dev") {                                          
                        echo "First Dev"
                    }   
                }
            }
        }
        stage('First Prod'){
            steps{
                echo "${env.GIT_BRANCH}"
                script{                
                    if (env.GIT_BRANCH == "origin/master") {                                          
                        echo "First Prod"
                    }   
                }
            }
        }
        stage('Second Dev'){
            steps{
                echo "${env.GIT_BRANCH}"
                script{                
                    if (env.GIT_BRANCH == "origin/dev") {                                          
                        echo "First Dev"
                    }   
                }
            }
        }
        stage('Second Prod'){
            steps{
                echo "${env.GIT_BRANCH}"
                script{                
                    if (env.GIT_BRANCH == "origin/master") {                                          
                        echo "First Prod"
                    }   
                }
            }
        }
    }
}