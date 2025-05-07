pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh'''
                    git clone https://github.com/alienated-forstbyte/hello-world
                    cd hello-world
                    sudo docker build -t hello-world .
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh'''
                    cd hello-world
                    sudo docker run --rm hello-world
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh'''
                    cd hello-world
                    docker run -d -p 8080:80 hello-world
                '''
            }
        }
    }
}
