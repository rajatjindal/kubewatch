pipeline {
  agent {
    docker {
      image 'golang:1.8.0'
    }
    
  }
  stages {
    stage('Compile') {
      steps {
        sh '''go get ./...
go build -o kubewatch main.go'''
      }
    }
  }
}