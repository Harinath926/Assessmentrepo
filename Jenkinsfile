pipeline {
    agent any 
    stages {
        stage('test') { 
            steps {
           echo "Hello world"  
            }
        }
        stage('Build') { 
            steps {
               echo "test"
           sh "sudo docker build -t my-app:1.0 ."
           sh "docker images"
            }
        }
        stage('Execute') { 
            steps {
              echo "deploy" 
           sh "sudo docker run my-app:1.0"
            }
        }
    }
}
