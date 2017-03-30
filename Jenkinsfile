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

dockerNode(image: "maven:3.3.3-jdk-8", sideContainers: ["selenium/standalone-firefox"]) {
  git "https://github.com/wakaleo/game-of-life"
  sh 'mvn clean test'
}
