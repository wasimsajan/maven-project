pipeline {
    agent any
    stages 
    {       
        stage ('SCM Checkout') {
          git url: 'https://github.com/prakashk0301/maven-project'
         }  
    }
    {
        stage ('Compile Stage') {
            when {
                branch "master"
            } 
            steps {
                withMaven(maven : 'localmaven') 
                {   
                    sh 'mvn compile' 
                }            
            }
    }      
  }
    { stage ('package') {
        when {
                branch "when-condition-ci-cd"
            } 
        steps {
                withMaven(maven : 'localmaven') 
                {   
                    sh 'echo hello' 
                }            
            }
    }
    }
}
