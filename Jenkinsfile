pipeline{
agent any
 environment{
        DOCKER_TAG = getDockerTag()
           }
stages{ 
 
 stage('checkout'){
  steps{
  
  git credentialsId: 'git', url: 'https://github.com/paul123-gif/docker1.git'
  }
 
 
 }
 
 
 
         stage('buiuld'){
             steps{
               sh 'docker build . -t paul1199/nodeapp:${DOCKER_TAG}'
                 }
          }
      }
}

def getDockerTag(){
    def tag  = sh script: 'git rev-parse HEAD', returnStdout: true
    return tag
}
