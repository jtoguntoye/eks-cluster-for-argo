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
                docker.build(joeltosin/eksapp)
            }
        }

    }
}