

pipeline
{
  agent any
  stages
  {
      stage ('scm checkout')
      {
          steps
          {
               git branch: 'master', url: 'https://github.com/wasim-sajan/maven-project'
          }
      }
      stage ('compile the code')
      {
          steps 
           {
              withMaven(jdk: 'local-java-1.8', maven: 'local-maven') 
              {
                 sh 'mvn compile'
              }
           }
      }
      stage ('package the code')
      {
          steps 
           {
              withMaven(jdk: 'local-java-1.8', maven: 'local-maven') 
              {
                 sh 'mvn compile'
              }
           }
      }
  }  
}
