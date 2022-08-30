pipeline {
    agent any
    
    tools {nodejs "node"}
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
         stage('Deliver') {
                            steps {
                                sh "chmod +x ./scripts/deliver.sh"
                                sh './scripts/deliver.sh'
                                input message: 'Finished using the Rat-in-maze app? (Click "Proceed" to continue)'
                                sh "chmod +x ./scripts/kill.sh"
                                sh './scripts/kill.sh'
                            }
                        }
            }
      }