pipeline {

  agent { label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/rengaprakashs/pipeline2.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "renga")
        }
      }
    }

  }

}
