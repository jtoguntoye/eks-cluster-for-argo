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

        stage('push image to Docker hub') {
            
            steps{
                script{
                    docker.withRegistry('https://registry.hub.docker.com', 'DOCKERHUBCREDENTIALS'){
                    app.push("${env.BUILD_NUMBER}")
                    }
                }
            }
        }

    }
}