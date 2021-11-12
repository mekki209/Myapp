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

 
      /*  stage('Install') {
             steps{
                script{
                    sh "sudo npm install"
                }
            }
        }*/
        
        stage('Build') {
             steps{
                script{
                    sh " ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml"
                }
            }
        }
     /*   stage('docker')
{
                  steps {
                         script{
                         sh "ansible-playbook Ansible/docker.yml -i Ansible/inventory/host.yml "
                                }
                        }
  }*/
      

}
}
