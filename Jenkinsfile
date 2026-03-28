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
                
                        sh '/usr/local/bin/kubectl apply -f pod1.yaml'
                        sh '/usr/local/bin/kubectl get pods'
                      
            }
            }

    }

}