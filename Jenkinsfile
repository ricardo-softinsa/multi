pipeline{
    agent any
    stages{
        stage('First Dev'){
            when{
                branch 'Dev'
            }
            steps{
                echo "First Dev"
            }
        }
        stage('First Prod'){
            when{
                branch 'master'
            }
            steps{
                echo "First Prod"
            }
        }
        stage('Second Dev'){
            when{
                branch 'Dev'
            }
            steps{
                echo "Second Dev"
            }
        }
        stage('Second Prod'){
            when{
                branch 'master'
            }
            steps{
                echo "Second Prod"
            }
        }
    }
}