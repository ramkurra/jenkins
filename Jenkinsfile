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
                sh 'echo "in Build" ' 
            }
        }

               stage('deploy'){
            steps{
               sh 'echo "in deploy" ' 
               sh 'echo "Git user is ${GIT_USER}"'
            }
        }
       
    }
    post{
        alwasys{
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