pipeline {
  agent none 
    
stages{ 
	stage('Build') { 
		agent { docker 'alpine:latest' }
        steps {
       	echo 'Building...'
        sh 'cat /etc/alpine-release'
      }
    }
    stage('Test') {
          agent { docker 'centos:latest' }
      steps {
        echo 'Testing... On Centos'
        sh 'cat /etc/centos-release'
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
