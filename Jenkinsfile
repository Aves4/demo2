pipeline{
  agent any
  environment{
    GIT_BRANCH: 'master'
    url: 'https://github.com/Aves4/demo2.git'
  }
  stages{
    stage(clone){
      steps{
        git branch:"${GIT_BRANCH}", "${url}"
      }
    }
    stage(compile){
      steps{
        sh 'mvn compile'
      }
    }
    stage(test){
      steps{
        sh 'mvn test'
      }
    }
    stage(build){
      steps{
        sh 'mvn clean install'
      }
    }
  }
}
      
  
