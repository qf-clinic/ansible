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
                sh 'ansible-playbook -i inventory.yml site.yml -e "portnumber=84"'
            } 
        }
    }
}
