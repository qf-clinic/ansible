pipeline {
    agent { label 'ansible-label' }

    // tools {
    //     maven "M3"
    // }

    stages {
        stage('clone') {
            steps { 
                checkout scm
            } 
        }
        stage('ansible') {
            steps { 
                ansible-playbook -i inventory.yml site.yml -e "portnumber=84"
            } 
        }
    }
}
