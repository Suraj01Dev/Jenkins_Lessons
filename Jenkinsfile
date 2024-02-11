pipeline{
    agent any
    environment{
        release=1.0.0
        username=<username>
        passid=<pass_id>
        appname=<app_name>
        image_name="${username}"+"/"+"${appname}"
        tag="${release}"+"-"+"${currentBuild.number}"
    }

    stages{
        stage("Docker build ")
        {
            sh
            '''
            docker build . -t "${image_name}:${tag}"
            '''
        }
    }
}
