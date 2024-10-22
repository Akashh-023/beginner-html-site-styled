pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t akashsharma2303/website .'
      }
    }
    stage('Push') {
      steps {
        sh 'docker push akashsharma2303/website'
      }
    }
    stage('Deploy') {
      steps {
        sh 'kubectl apply -f deployment.yaml'
        sh 'kubectl apply -f service.yaml'
      }
    }
  }
}
