pipeline{
    agent any

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

                  def app = docker.build("joeltosin/eksapp")
                }
                
            }
        }

    }
}