pipeline {
    agent any

    stages {
        stage('Execute Ansible Play') {
            steps {
                wrap([$class: 'AnsiColorBuildWrapper', colorMapName: "xterm"]) {
				ansiblePlaybook(
					playbook: "${WORKSPACE}/ansible/plays/demoplays.yml",
					inventory: "${WORKSPACE}/ansible/inventory/hosts.yml",
					extras: "-u devops",
					extraVars: [
						jenkins_workspace: "${WORKSPACE}"
				)
			}
            }
        }
    }
}