pipeline{
    
    agent any
    environment{
        JENKINS_HOME="/var/jenkins_home"
        USER="ramkurra"
    }
    credentials{
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
 
}