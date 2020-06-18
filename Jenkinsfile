pipeline{
agent any
 environment{
        DOCKER_TAG = getDockerTag()
           }
stages{ 
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
