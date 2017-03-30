pipeline{
  agent any
  stages{
    stage('Test'){
      steps{
        sh 'pytest'
      }
    }
    stage('Run'){
      steps{
        sh 'python3 app.py'
      }
    }
  }
}
