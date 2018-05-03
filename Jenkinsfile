pipeline {
  agent any
  stages {
    stage('Deploy Standalone') {
      steps {
        bat 'clean install deploy -P standalone'
      }
    }
  
      stage('Deploy ARM') {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        bat 'clean install deploy -P arm -Darm.target.name=apprhel74mupoc08i -Danypoint.username=bimehta -Danypoint.password=Mel2018a'
      }
    }
    stage('Deploy CloudHub') {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        bat 'clean install deploy -P cloudhub -Dmule.version=3.9.0 -Danypoint.username=bimehta -Danypoint.password=Mel2018a'
      }
    }
  }
}
