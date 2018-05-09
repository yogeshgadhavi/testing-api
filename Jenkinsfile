pipeline {
  agent any
  stages {
     
     stage('Deploy ARM') {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
      steps {
        bat 'mvn deploy -P arm -Darm.target.name=local-3.9.0-ee -Danypoint.username=bimehta -Danypoint.password=Mel2018a'
      }
    }
    
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
