 pipeline{
 agent any
 stages{
 stage('code checkout'){
  steps{
       git branch: 'main', credentialsId: 'gitCredentials', url: 'https://github.com/shashikanth-t/jenkins-ansible.git'
       }
 }
 stage('Execute Ansible'){
  steps{
     ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, inventory: 'dhost.inv', playbook: 'apache.yml'  
      }
    }
}
}
