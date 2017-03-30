pipeline{
  agent any
  stages{
    stage('Test'){
      steps{
        echo 'Hi'
      }
    }
    stage('Run'){
      steps{
        sh 'python3 app.py'
      }
    }
  }
}
