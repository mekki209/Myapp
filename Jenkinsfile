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


stage('build')
{
                  steps {
                         script{
                         sh "ansible-playbook my-app/Ansible/build.yml -i my-app/Ansible/inventory/host.yml "
                                }
                        }
  }


}
}
