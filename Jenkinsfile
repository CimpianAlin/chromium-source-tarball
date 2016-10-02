timestamps {
  node {
    stage('Checkout') {
      checkout scm
    }
    stage('Boostrap') {
      sh 'script/bootstrap'
    }
    stage('sync') {
      sh 'script/sync ${env.CHROMIUM_VERSION}'
    }
    stage('upload') {
      sh 'script/upload'
    }
  }
}
