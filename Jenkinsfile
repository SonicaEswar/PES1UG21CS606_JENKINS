pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'cd main && g++ -o a hello.cpp'
        build 'PES1UG20CS606-1'
        echo 'build stage successfull'
      }
    }
    stage('Test'){
      steps{
        sh 'cd main && ./a'
        echo 'test stage sucessfull'
      }
    }
    stage('Deploy'){
      steps{
        mh 'deploy'
        echo 'Deply stage sucessfull'
      }
    }
  }
  post{
    always{
      echo 'pineline is successfull'
    }
    failure{
      echo 'pipeline falied'
    }
  }
}
