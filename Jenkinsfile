pipeline{
	agent{label 'ansible'}
	stages{
		stage('SCM Checkout'){
			steps{
				git 'https://github.com/srikanta1219/shanvi-jenkins-ansible.git'
			}
		}
		stage('Execute Ansible'){
			steps{
				ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'ansible-master', inventory: 'dev.inv', playbook: 'apache.yml'
			}
		}
	}
}
