pipeline{
      agent any
      tools{
            nodejs 'NodeJs22'
      }
      stages{
            stage('Install Dependencies'){
                  steps{
                        sh 'npm install'

                  }
            }
            stage("Build Phase"){
                  steps{
                        sh 'npm run build'
                  }
            }
      }
      post{
            success{
                  echo "successfully completed Install and build"
            }
            failure{
                  echo "failed due to some reason"
            }
            always{
                  echo 'pipeline finished'
            }
      }
}