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
