pipeline{
    
    agent any
    environment{
        JENKINS_HOME="/var/jenkins_home"
        USER="ramkurra"
         GIT_USER=credentials( 'GitRepoRK')
    }
   
    stages{

        stage('init'){
            steps{
               sh '''
               echo "in Init" 
               echo "jenkins home is ${JENKINS_HOME}"
               echo "USER is ${USER}"
               '''
            }
        }
           stage('build'){
            steps{
               sh 'echo "in Build" ' 
            
            }
        }
        stage('test'){
            when{
                expression{
                    env.BRANCH_NAME=='testmulti'
                }
            }
            steps{
               sh 'echo "in test" ' 
             
            }
        }

               stage('deploy'){
            steps{
               sh 'echo "in deploy" ' 
               sh 'echo "Git user is ${GIT_USER}"'

               withCredentials([
                   usernamePassword(credentialsId: 'GitRepoRK', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')
               ]){
                   sh 'echo "User is ${USERNAME} and password is ${PASSWORD}"'
               }
            }
        }
       
    }
    post{
        always{
            sh 'echo "in always " ' 
        }
        success{
            sh 'echo "in success" ' 
        }
        failure{
            sh 'echo "in failure" ' 
        }
    }
 
}