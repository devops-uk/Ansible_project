pipeline {
    agent any

    stages {
        stage('Run Ansible Playbook') {
            steps {
                sh '''
                  export ANSIBLE_HOST_KEY_CHECKING=False
                  ansible-playbook \
                    -i inventory.ini \
                    install-nginx.yml \
                    --become --become-method=sudo
                '''
            }
        }
    }
}

