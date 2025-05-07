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
          withDockerRegistry(credentialsId: 'docker-pass'){
            sh'''
            docker build -f hello-python .
            '''
          }
        }
      }
    }
  }
      
}
