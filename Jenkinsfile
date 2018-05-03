pipeline {
  agent any
  stages {
    stage('Deploy Standalone') {
      steps {
        bat 'mvn deploy -P standalone'
      }
    }
    stage('Deploy ARM') {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        bat 'mvn deploy -P arm -Darm.target.name=apprhel74mupoc08i -Danypoint.username=bimehta -Danypoint.password=Mel2018a'
      }
    }
    stage('Deploy CloudHub') {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        bat 'mvn deploy -P cloudhub -Dmule.version=3.9.0 -Danypoint.username=bimehta -Danypoint.password=Mel2018a'
      }
    }
  }
}
