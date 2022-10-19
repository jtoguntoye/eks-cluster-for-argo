pipeline{
    agent any

    stages{
        stage('Checkout source'){
            steps{
                sh 'echo hello world'
                chckout scm
            }
        }
        // stage('build image') {
        //     steps{
        //         docker.build(joeltosin/eksapp)
        //     }
        // }
    }
}