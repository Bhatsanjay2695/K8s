pipeline
{
    agent any
    environment {
        PATH = "/usr/local/bin:/opt/homebrew/bin:${env.PATH}"
    }
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
        sh 'echo $PATH'
        sh 'which docker'
        sh 'docker version'

            echo 'checking the prereqss'
            sh ' /opt/homebrew/bin/docker version | grep -q "Server" && echo "docker installed" || open -a Docker'
            sh ' /opt/homebrew/bin/kind get clusters | grep -q "kind" && echo "kind installed already" || /opt/homebrew/bin/kind create cluster'
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