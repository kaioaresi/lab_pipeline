pipeline {
  agent any
  stages {
    stage('Build image') {
      steps {
        sh 'docker build -t kaioaresi/jenkins:${TAG_DEV} .'
      }
    }
    stage('Deploy') {
      steps {
        sh '''#docker stack deploy -c docker-compose.yml ${JOB_NAME}-QA

echo $JOB_BASE_NAME'''
      }
    }
  }
}