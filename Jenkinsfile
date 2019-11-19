node {
   
   stage('Code Checkout') { // for display purposes
      // Get some code from a GitHub repository
      git credentialsId: 'gitID', url: 'https://github.com/itrainOrg/jenkins-docker.git'
     
   }
   stage('Docker Build') {
     def app = docker.build "amritasthampi/itrainorg-jenkin-dkr"
    }
   stage('Tag & Push') {
      withDockerRegistry(credentialsId: 'dockerID', url: '') {
        sh 'docker tag amritasthampi/itrainorg-jenkin-dkr amritasthampi/itrainorg-jenkin-dkr:dev'
        sh 'docker push amritasthampi/itrainorg-jenkin-dkr:dev'
        sh 'docker push amritasthampi/itrainorg-jenkin-dkr:latest'
      }
   }
   stage('Results') {
       echo 'deploy to docker hub is succesfull'
      
   }
}
