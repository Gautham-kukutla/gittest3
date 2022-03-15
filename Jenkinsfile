pipeline{
agent any
  stages{
  stage('Testing webhook'){
  steps{
    echo "Jenkins in dev branch"
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
 }
}
