pipeline {
  agent any
  parameters {
    booleanParam(name: "isDeployPod", defaultValue: true)
  }
  stages {
    stage('abc') {
      when {
        expression {
          params.isDeployPod
        }
      }
      steps {
        sh 'kubectl apply -f deploy.yml --kubeconfig  /jenkins-kube/admin.conf'
      }
    }
    post {
      success {
        echo "all good :))"
      }
      failure {
        echo "something failed  :(("
      }
      always {
        echo "always :<|"
      }
    }
  }
}
