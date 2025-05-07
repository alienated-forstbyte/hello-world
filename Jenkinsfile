pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        echo 'Building...'
        sh '''
                    git pull https://github.com/alienated-forstbyte/hello-world.git
                    su root
                    cd hello-world
                    docker build -t hello-world .
                '''
        git(url: 'https://github.com/alienated-forstbyte/hello-world', branch: 'master')
      }
    }

    stage('Test') {
      steps {
        echo 'Testing...'
        sh '''
                    cd hello-world
                    sudo docker run --rm hello-world
                '''
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying...'
        sh '''
                    cd hello-world
                    docker run -d -p 8080:80 hello-world
                '''
      }
    }

  }
}