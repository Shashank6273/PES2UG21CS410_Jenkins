pipeline {
  agent any 
  stages {
//   stage('Clone repository') {
//      steps {
//        checkout ([$class: 'GitSCM', 
//        branches: [[name: '*/main']], 
//        userRemoteConfigs: [[url: 'https://github.com/Shashank6273/PES2UG21CS410_Jenkins.git']]})
//        }
//   }
      stage( 'Build') {
        steps {
          build 'pes2ug21cs410-1'
          sh 'g++ main.cpp -o output'
      }
    }
      stage ('Test') {
        steps {
          sh './output'
      }
    }
      stage ('Deploy') {
        steps {
          echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }

