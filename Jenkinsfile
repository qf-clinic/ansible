pipeline {
    agent { label 'ansible-label' }
    stages {
        stage('clone') {
            steps { 
                checkout scm
            } 
        }
        stage('ansible') {
            steps { 
                sh 'sudo -i'
                sh 'whoami'
                sh 'ansible-playbook -i inventory.yml site.yml -e "portnumber=84"'
            } 
        }
    }
}
