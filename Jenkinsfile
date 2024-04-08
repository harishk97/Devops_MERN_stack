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

    // stage('Build image') {
    //   steps{
    //     script {
    //       dockerImage = docker.build dockerimagename
    //     }
    //   }
    // }

    // stage('Pushing Image') {
    //   environment {
    //            registryCredential = 'dockerhublogin'
    //        }
    //   steps{
    //     script {
    //       docker.withRegistry( 'https://registry.hub.docker.com', registryCredential ) {
    //         dockerImage.push("latest")
    //       }
    //     }
    //   }
    // }

    stage('Deploying App to Kubernetes') {
      steps {
        withKubeConfig(caCertificate: '', clusterName: 'minikube', contextName: '', credentialsId: 'k8s-cred', namespace: '', restrictKubeConfigAccess: false, serverUrl: 'https://192.168.49.2:8443') {
              sh "kubectl get pods"
          }
        }
      }
    } 
}
