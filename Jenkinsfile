pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'g++ main/hello.cpp -o run'
        hello 'Successfully compiled hello'
      }
    }
    stage('Test'){
      steps{
        sh './run'
      }
    }
    stage('Deploy'){
      steps{
        echo "Deployed"
      }
    }
  }
  post{
    failure{
      echo "Pipeline Failed!"
    }
  }
}
