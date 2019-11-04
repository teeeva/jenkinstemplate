pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        echo 'Building...'
        sh '''     echo "Database engine is ${DB_ENGINE}"


                echo "DISABLE_AUTH is ${DISABLE_AUTH}"'''
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }
  }
  environment {
    DB_ENGINE = 'sqlite'
    agent = 'docker'
  }
}