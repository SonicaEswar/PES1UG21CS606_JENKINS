pipeline{
  agent any
  stages {
//       stage ('Clone repository') {
//           steps{
//               checkout([$class: 'GitSCM',
//               branches: [[name: '*/main]],
//               userRemoteConfigs: [[url:'https://github.com/SonicaEswar/PES1UG21CS606_JENKINS.git']]])
//           }
//        }
    stage('Build'){
      steps{
        build 'PES1UG21CS606-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
