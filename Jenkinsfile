pipeline {

/*  environment {
    dockerimagename = "thetips4you/nodeapp"
    dockerImage = ""
  }
*/
  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git branch: 'main', url: 'https://github.com/harishk97/Devops_MERN_stack.git'
      }
    }
/*
    stage('Build image') {
      steps{
        script {
          dockerImage = docker.build dockerimagename
        }
      }
    }

    stage('Pushing Image') {
      environment {
               registryCredential = 'dockerhublogin'
           }
      steps{
        script {
          docker.withRegistry( 'https://registry.hub.docker.com', registryCredential ) {
            dockerImage.push("latest")
          }
        }
      }
    }

    stage('Deploying App to Kubernetes') {
      steps {
        script {
          kubernetesDeploy(configs: "secret.yml", kubeconfigId: "kubernetes")
          kubernetesDeploy(configs: "mongo-config.yml", kubeconfigId: "kubernetes")
          kubernetesDeploy(configs: "db_mongo_app.yml", kubeconfigId: "kubernetes")
          kubernetesDeploy(configs: "db_service.yml", kubeconfigId: "kubernetes")
          kubernetesDeploy(configs: "web-app.yml", kubeconfigId: "kubernetes")
          kubernetesDeploy(configs: "webapp-service.yml", kubeconfigId: "kubernetes")
        }
      }
    } */
}
}
