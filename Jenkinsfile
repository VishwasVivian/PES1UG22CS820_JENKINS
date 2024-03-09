pipeline{
  agent any
  stages{
          // stages('Clone repository'){
          //       steps{
          //             checkout([$class: 'GitSCM',
          //             branches: [[name: '*/main']],
          //             userRemoteConfigs: [[url: 'https://github.com/VishwasVivian/PES1UG22CS852_JENKINS.git']]])
          //               }
          //         }
          stage('Build'){
                steps{
                      build 'PES1UG22CS820-1'
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
