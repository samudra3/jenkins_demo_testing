pipeline{
      agent any
      tools{
            nodejs 'NodeJs22'
      }
      stages{
            stage('Inspect env'){
                  steps{

                        sh 'which node || true'
                        sh 'node -v'
                        sh 'which npm || true'
                        sh 'npm -v'
                  }
            }
      }
      post{
            always{
                  echo 'pipeline finished'
            }
      }
}