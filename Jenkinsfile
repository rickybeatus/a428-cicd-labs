node {
  stage('Build') {
    docker.image('node:lts-bullseye-slim').inside {
      sh 'npm install'
    }
  }
  stage('Test') {
    docker.image('node:lts-bullseye-slim').inside {
      sh './jenkins/scripts/test.sh'
    }
  }
}