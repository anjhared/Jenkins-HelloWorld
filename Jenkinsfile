node {
    stage('Execute Ansible Play') {
        ansiblePlaybook(
            playbook: "${WORKSPACE}/ansible/plays/demoplays.yml",
			inventory: "${WORKSPACE}/ansible/inventory/hosts.yml",
            colorized: true,
			extras: "-u devops",
			    extraVars: [
				    jenkins_workspace: "${WORKSPACE}"
		)
    }
}