pipeline {
    agent any
      stages{
         stage('Pull'){
            steps {
              script{
                  checkout([$class: 'GitSCM', branches: [[name: '*/main']],
                       userRemoteConfigs: [[
                          credentialsId:'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',
                          url: 'https://github.com/mekki209/Myapp.git']]])

                     }

            }
        }
        }
        }
