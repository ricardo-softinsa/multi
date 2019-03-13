pipeline{
    agent any
    stages{
        stage('First Dev'){
            steps{
                echo bat(returnStdout: true, script: 'set')
                echo "Something new"
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
                echo "Something new"
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
                        echo "Second Dev"
                    }   
                }
            }
        }
        stage('Second Prod'){
            steps{
                echo "${env.GIT_BRANCH}"
                script{                
                    if (env.GIT_BRANCH == "origin/master") {                                          
                        echo "Second Prod..."
                    }   
                }
            }
        }
    }
}