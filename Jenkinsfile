pipeline{
  agent any
  
  environment{
    git_branch: 'master'
    url: 'https://github.com/Aves4/demo2.git'
  }
  stages{
    stage(clone){
      steps{
        git branch:"${git_branch}", url:"${url}"
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
      
  
