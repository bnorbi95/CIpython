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
  git "https://github.com/wakaleo/game-of-life"
  sh 'mvn clean test'
}
