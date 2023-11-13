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
        
       stage('SONARQUBE') {
            steps {
                dir('DevOps_Project') {
                sh 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.login=admin -Dsonar.password=0000'
            }
            }
        }
      stage('NEXUS') {
            steps {
                dir('DevOps_Project') {
                sh 'mvn clean deploy -DskipTests'
            }
            }
        }
        

}
}




