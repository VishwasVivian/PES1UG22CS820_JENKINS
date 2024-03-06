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
          stages('Build'){
                steps{
                      build 'PES1UG22CS852-1'
                      sh 'g++ main.cpp -o output'
                  }
          }
          stages('Test'){
                steps{
                      sh './output'
                  }
          }
          stages('Deploy'){
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
