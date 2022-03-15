pipeline {
agent any
  stages {
  stage('Testing webhook'){
  steps{
    echo "Jenkins in master"
  }}
    stage ('test') {
        when {
            expression{
            GIT_BRANCH == 'dev'
            }
        }
        steps {
             echo 'Test stage dev is executed.'
        }}
        stage ('Deploy') {
        when {
            expression{
           BRANCH_NAME == 'master'
            }}
        steps {
             echo 'Test stage Master is executed.'
        }
    }
  }post { 
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
        }}
}
