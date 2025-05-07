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
    stage('Build DOcker Image'){
      steps{
        script{
          sh'''
          docker build -f hello-python .
          '''
        }
      }
    }
  }
      
}
