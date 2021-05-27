pipeline {
  agent any
  stages {
    stage('abc') {
      steps {
        sh 'kubectl apply -f deploy.yaml --kubeconfig /jenkins-kube/admin.conf'
      }
    }
  }
}
