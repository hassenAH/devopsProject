pipeline {
    agent any
    tools{
        nodejs 'nodejs'
    }
    
    stages {
        stage('GIT') {
            steps {
                checkout scm
            }
        }

         
     
       stage(' UNIT TESTES AND NOTIF') {
            steps {
                dir('DevOps_Project') {
                    script {
                        try {
                            sh 'mvn clean install'
                        } catch (Exception e) {
                            currentBuild.result = 'FAILURE'
                            error("Build failed: ${e.message}")
                        }
                    }
                }
            }
           
        }
       
}
}




