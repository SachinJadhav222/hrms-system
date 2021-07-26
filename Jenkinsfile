pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'This is Build Stage'
          }
        }

        stage('sonar') {
          steps {
            echo 'Sonar analysis'
            sh '''echo "This is SONAR Test"
ls -la'''
          }
        }

      }
    }

    stage('test') {
      steps {
        echo 'Test running ...'
        sh '''echo "This is Test stage"
pwd'''
      }
    }

    stage('deploy') {
      steps {
        echo 'deploy....'
        sh '''echo "Thsi is Delpoy......"
ls -a'''
      }
    }

  }
}