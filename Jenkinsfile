pipeline{
    agent any
    environment{
        PATH = "/usr/bin/mvn:$PATH"
    }
    stages{
        stage("SCM"){
            steps{
                git credentialsId: 'git_credentials', url: 'https://github.com/nikhil-arella/valaxy-hello-world.git'
            }
        }
        stage("build"){
            steps{
                sh "mvn clean install"
            }
        }
    }
}
