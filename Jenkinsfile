node {
   
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git credentialsId: 'githubID', url: 'https://github.com/itrainpulsars/jenkins-docker.git'
     
   }
   stage('Docker Build') {
     def app = docker.build "manee2k6/pulsar-jenkin-dkr"
    }
   stage('Tag & Push') {
      withDockerRegistry(credentialsId: 'dockerID', url: '') {
        sh 'docker tag manee2k6/pulsar-jenkin-dkr manee2k6/pulsar-jenkin-dkr:dev'
        sh 'docker push manee2k6/pulsar-jenkin-dkr:dev'
        sh 'docker push manee2k6/pulsar-jenkin-dkr:latest'
      }
   }
   stage('Results') {
       echo 'deploy to docker hub is succesfull'
      
   }
}
