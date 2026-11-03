pipeline {
    agent any

    stages {
        stage('Pre-Patching Health Check') {
            steps {
                sh '''
                    ansible-playbook -i inventory.ini health_check.yml
                '''
            }
        }

        stage('Automated Security Patching') {
            steps {
                sh '''
                    ansible-playbook -i inventory.ini automated_patching.yml
                '''
            }
        }
    }
}
