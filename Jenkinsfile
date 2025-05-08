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
            sh 'echo "48c0f60467c1457894fb2040e03507e6" | sudo -S docker build -t hellopython .'
          
        }
      }
    }
  }
}
