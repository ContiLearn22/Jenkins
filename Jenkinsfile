pipeline{
    agent {  node{ label "build01"}}


    stages{
        stage("build"){
            steps{
                script{
                    mvnHome = tool "M2"
                    sh "${mvnHome/bin/mvn -v}"
                   }
                }
            }
          }
}                                                                                                 
