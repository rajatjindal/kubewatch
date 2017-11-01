pipeline {
  agent {
    docker {
      image 'golang:1.8.0'
    }
    
  }
  stages {
    stage('Compile') {
      agent {
        docker {
          image 'golang:1.8'
        }
        
      }
      steps {
        sh '''go get ./...
go build -o kubewatch main.go'''
        sh 'whoami'
      }
    }
  }
}