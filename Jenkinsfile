pipeline{
      agent any
      environment{
            VERCEL_TOKEN = credentials('vercel_id')
      }
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
            stage("Deploy Phase"){
                  steps{
                        sh '''
                            npx vercel deploy \
                            --prod \
                            --token $VERCEL_TOKEN \
                            --yes
                            '''

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
