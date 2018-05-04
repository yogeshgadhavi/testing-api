pipeline {
  agent any
  stages {
          
      stage('Deploy CloudHub') {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        bat 'mvn install deploy -P cloudhub -Dmule.version=3.9.0 -Danypoint.username=bimehta -Danypoint.password=Mel2018a'
      }
    }
  }
}
