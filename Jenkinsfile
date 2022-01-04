currentBuild.displayName = "Test_build-#" + currentBuild.number
pipeline{
    environment{
        PATH = "/usr/share/maven/bin:$PATH"
    }
     agent any
     stages{
         stage("Gitcheckout"){
             steps{
             git branch: 'main', url: 'https://github.com/rapsurgy/docker_sample'
             }
         }
         stage("Maven Build"){
             steps{
                 sh "mvn clean package"
             }
         }
     }
}