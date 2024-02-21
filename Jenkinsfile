pipeline{
    agent {  node{ label "build01"}}


    stages{
        stage("mavenbuild"){
            steps{
                script{
                    mvnHome = tool "M2"
                    sh "${mvnHome}/bin/mvn -v"
                   }
                }
            }
          
        stage("ANTbuild"){
            steps{
                script{
                    try{
                    antHome = tool "ANT"
                    sh "${antHome}/bin/ant -v"}
                    catch(e){
                        println(e)
                    }
                }
            }
        }
        stage("GradleBuilf"){
            steps{
                script{
                    gradleHome = tool "GRADLE"
                    sh "${gradleHome}/bin/gradle -v"
                }
            }
        }
    }
}                                                                                                 
