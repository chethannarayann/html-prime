pipeline {
  agent any
  stages {
    stage('fetchFetch code ') {
      steps {
        git(url: 'git@github.com:chethannarayann/html-prime.git', poll: true, branch: 'main')
        git(url: 'https://github.com/chethannarayann/html-prime.git', branch: 'main', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}