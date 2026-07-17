pipeline{
      agent any
      stages{
            stage('Inspect env'){
                  steps{
                        sh 'pwd'
                        sh 'whoami'
                        sh 'echo $PATH'
                        sh 'which java'
                        sh 'which git'
                        sh 'which node || true'
                        sh 'which npm || true'
                  }
            }
      }
}