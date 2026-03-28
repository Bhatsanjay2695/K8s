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
                        sh 'whoami'
                        sh 'kubectl apply -f pod1.yaml'
                        sh 'kubectl get pods'
                      
            }
            }

    }

}