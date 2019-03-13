pipeline{
    agent any
    stages{
        stage('First Dev'){
            steps{
                checkout scm
                echo bat(returnStdout: true, script: 'set')
                echo "Something new"
                echo "${env.GIT_BRANCH}"
                script{         
                    def tag = sh(returnStdout: true, script: "git tag --contains | head -1").trim()  
                    if(tag){
                        echo "----------------"
                        echo "This\nis\njust\na\ntest"
                        echo "----------------"
                    }   
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
            when{
                tag "release3"
            }
            steps{
                echo "${env.GIT_BRANCH}"
                script{                
                    if (env.GIT_BRANCH == "origin/master") {                                          
                        echo "Second Prod"
                    }   
                }
            }
        }
    }
}