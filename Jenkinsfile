pipeline{
  agent any
  stages{
//    stage('Clone Repository'){
//      steps{
//        checkout([$class:'GitSCM',
//                  branches: [[ name:'*/main']],
//                              userRemoteConfigs: [[url: 'https://github.com/Mystery510/Shreeja_Rajesh_Jenkins.git' ]]])
//      }
//    }
    stage('Build'){
      steps{
        build 'PES1UG21CS564-1'
        sh 'g++ hello.cpp -o output'
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
