pipeline {
  agent any
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
            sh 'sudo docker build -t hellopython . -s W9e87jW97o$8f34'
          
        }
      }
    }
  }
}
