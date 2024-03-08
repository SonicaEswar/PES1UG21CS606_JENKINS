pipeline{
  agent any 
  stages {
    stage('Build'){
      steps{
        sh 'cd main  && g++ working.cpp'
        echo 'Build success'
      }
    
    }
    stage('Test'){
      steps{
        sh 'cd main && ./a.out'
        echo 'Test success'
      }
    }
  }
  post{
    failure{
      echo 'pipeline failed'
    }
  }
}
