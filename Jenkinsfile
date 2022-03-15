pipeline {
 agent any
  
  stages {
    stage('Start'){
      steps{
        echo "Jenkins in master"
  } }
    stage ('dev branch test') {
        when {
            expression{
            GIT_BRANCH == 'dev'
            }
        }
        steps {
             echo 'Test stage dev is executed.'
        } }
        stage ('master branch test') {
        when {
            expression{
           BRANCH_NAME == 'master'
            } }
        steps {
             echo 'Test stage Master is executed.'
        }
    }
  }
  post { 
        always { 
            echo 'This is post always'
        }
    failure { 
            echo 'This is post failure'
        }
    unsuccessful{
        echo 'this is post unsuccessful'
    }
    success { 
            echo 'This is post success'
        } }
}
