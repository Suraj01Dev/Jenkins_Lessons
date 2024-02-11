pipeline{
    agent {
        label "jenkins-ssh-agent-docker"
    }
    environment{
        release="1.0.0"
        username="suraj01dev"
        passid="dockerhub"
        appname="stock_app"
        image_name="${username}"+"/"+"${appname}"
        tag="${release}"+"-"+"${currentBuild.number}"
    }

    stages{
        stage("Docker build ")
        {
            steps
            {
            sh
            '''
            docker build . -t "${image_name}:${tag}"
            '''
            }
        }
    }
}
