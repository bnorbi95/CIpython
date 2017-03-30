pipeline{
  agent any
  stages{
    stage('Test'){
      steps{
        sh 'py.test'
      }
    }
    stage('Run'){
      steps{
        sh 'python3 app.py'
      }
    }
  }
}

dockerNode(image: "ubuntu:16.04") {
  git "https://github.com/bnorbi95/CIpython.git"
  sh 'apt-get update && apt install -y python-logilab-common'
  sh 'py.test'
}
