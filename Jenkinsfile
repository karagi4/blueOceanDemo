pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is Build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to Dev_1') {
          steps {
            echo 'finished'
          }
        }

        stage('Deploy to Dev_2') {
          steps {
            sleep 50
            echo 'completed'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'testing...'
      }
    }

  }
}