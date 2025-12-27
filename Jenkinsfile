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
                        sh 'kubectl apply -f replicaset.yaml'
                        sh 'kubect port-forward rc-bharaths 8090:80'
            }
            }

    }

}