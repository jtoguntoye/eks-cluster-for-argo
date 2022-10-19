pipeline{
    agent any
    def app

    stages{
        stage('view code source'){
            steps{
                sh 'echo hello world'
                sh "cat ./Dockerfile"
                
            }
        }
        stage('build image') {
            steps{
                script{
                  app = docker.build(joeltosin/eksapp)
                }
                
            }
        }

    }
}