pipeline {
    agent {
  label 'ansible'
    }
    stages {
        stage('Check') { 
            steps {
                sh 'pip3 install "molecule==3.5.2" "molecule_docker"'
                sh "docker pull aragast/netology:latest"
            }
        }
        stage('Build') {
            steps {
                sh 'cd /root/p7-office && molecule test -s default'
            }
        }
    }
}
