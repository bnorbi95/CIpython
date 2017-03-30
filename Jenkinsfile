pipeline{
  agent any
  stages{
    stage('Test'){
      steps{
        dockerNode(image: "ubuntu:16.04") {
          git "https://github.com/wakaleo/game-of-life"
          sh 'mvn clean test'
        }
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
