pipeline
{
    agent any
    stages
    {
        stage('checkout')
        {
            steps
            {
            echo 'came to SCM'
            checkout scm
            }
        }
        stage('test')
        {
            steps
            {
            echo 'checking the prereqss'
            sh ' docker version | grep -q "Server" && echo "docker installed" || open -a Docker'
            sh ' kind get cluster | grep -q "kind v0." && echo "kind installed already" || kind create cluster kindk8'
            }    
        }
        stage('deployment')
        {
            steps
            {
            echo 'deployment of the k8'
            sh '/usr/local/bin/kubectl apply -f pod1.yaml'
            }

        }

    }

}