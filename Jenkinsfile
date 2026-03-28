pipeline
{
    agent any
    stages
    {
            stage('checkout')
            {
                steps{
                echo 'clonning the code'
                checkout scm
            }
            }
            stage('deploy and host the website')
            {
                steps{
                        sh 'which kubectl'
                        sh 'kubectl get pods'
                      
            }
            }

    }

}