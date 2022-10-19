pipeline{
    agent any

    environment {
		DOCKERHUBCREDENTIALS=credentials('DOCKERHUBCREDENTIALS')
	}

    stages{
        stage('build image') {
            steps{
                script{
                   def app = docker.build("joeltosin/eksapp:${env.BUILD_NUMBER}")
                }  
            }
        }

        stage('push image to Docker hub') {
            steps{
				sh 'echo $DOCKERHUBCREDENTIALS_PSW | docker login -u $DOCKERHUBCREDENTIALS_USR  --password-stdin'
				sh "docker push joeltosin/eksapp:${env.BUILD_NUMBER}"
		    	}               
        }
         

    }
}