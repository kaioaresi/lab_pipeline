pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t kaioaresi/jenkins_teste:${tag_img} .'
      }
    }
    stage('Push image') {
      steps {
        sh 'docker login -u ${DOCKER_USERNAME} -p "${DOCKER_PASSWORD}"'
        sh 'docker push kaioaresi/jenkins_teste:${tag_img}'
      }
    }
  }
  environment {
    tag_img = 'development'
  }
}