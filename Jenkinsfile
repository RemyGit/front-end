pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test job'
        sh 'npm install'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'npm install'
        sh 'npm run package'
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'NodeJS 4.8.6'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}
