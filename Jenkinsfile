node {
    stage('Execute Ansible Play') {
        wrap([$class: 'AnsiColorBuildWrapper', colorMapName: "xterm"]) {
            ansiblePlaybook(
                playbook: "${WORKSPACE}/ansible/plays/demoplays.yml",
		    	inventory: "${WORKSPACE}/ansible/inventory/hosts.ini",
                colorized: true,
		    	extras: "-u devops",
			        extraVars: [
			    	    jenkins_workspace: "${WORKSPACE}"
		    )
        }
    }
}