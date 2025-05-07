pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git url:'https://github.com/alienated-forstbyte/hello-world', branch:'master'
      }
    }
    stage('Run Test'){
      steps {
        sh 'python your_script.py'
      }
    }
  }
      
}
