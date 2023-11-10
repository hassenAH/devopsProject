pipeline {
    agent any
   /*  tools{
        nodejs 'DevOpsfrontend'
    }*/
    
   /*environment {
    DOCKERHUB_CREDENTIALS = credentials('dockerhubpwd')
    }*/
    
    stages {
        stage('GIT') {
            steps {
                checkout scm
            }
        }

         
     
       /* stage(' UNIT TESTES AND NOTIF') {
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
           
        }*/
        
       /*stage('SONARQUBE') {
            steps {
                dir('DevOpsBackend-main') {
                sh 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000 -Dsonar.login=admin -Dsonar.password=0000'
            }
            }
        }*/
      /*stage('NEXUS') {
            steps {
                dir('DevOpsBackend-main') {
                sh 'mvn clean deploy -DskipTests'
            }
            }
        }*/
        
           /* stage('BBUILD FRONT') {
                steps {
                    dir('DevOps_Project_Front') {
                        script {
                            
                            sh 'npm install -g npm@latest'
                            sh 'npm install --force'
                            sh 'npm run build'      
                        }
                    }
                }
            }*/

      /*stage('LOGIN DOCKER') {
        steps {
        script {
            withCredentials([string(credentialsId: 'password', variable: 'dockerhubpwd')]) {
            sh 'docker login -u monaemhamila -p ${dockerhubpwd}'
                }
            }
        }    
      }

        stage('CREATE DOCKER IMAGE BACK') {
            steps {
                dir('DevOps_Project') {
                    script {
                        sh 'docker build -t monaemhamila/devopsbackend .'
                        sh 'docker push monaemhamila/devopsbackend'
                    }
                }
            }
        }
        stage('CREATE DOCKER IMAGE FRONT') {
            steps {
                dir('DevOps_Project_Front') {
                    script {
                        sh 'docker build -t monaemhamila/devopsfrontend .'
                        sh 'docker push monaemhamila/devopsfrontend'
                        
                    }
                }
            }
        }
        
       stage('DEPLOY APP') {
            steps {
                
                script {
                    sh 'docker-compose -f docker-compose.yml up -d' 
                    sh 'docker-compose -f docker-compose.yml start'                       
                }
                
            }
        }*/
}
}




