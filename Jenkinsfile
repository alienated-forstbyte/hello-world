pipeline {
  agent any

  environment{
    PASSWORD = 'W9e87jW97o$8f34'
  }
  stages {
    stage('Checkout Code') {
      steps {
        git url:'https://github.com/alienated-forstbyte/hello-world.git', branch:'master'
      }
    }
    stage('Run Test'){
      steps {
        sh 'python hello.py'
      }
    }
    stage('Build Docker Image'){
      steps{
        script{
          //sh 'echo \'W9e87jW97o$8f34\' | sudo -S '
          //dockerImage = docker.build("hellopython")
            sh 'echo \'W9e87jW97o$8f34\' | sudo -S docker build -t hellopython .'
          
        }
      }
    }
  }
}
