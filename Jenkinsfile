node() 
{

stage("Clone"){

    git "https://github.com/marionschlotte/hana-shine-xsa.git"

}


stage("Build")
{
    
sh "java -jar /var/jenkins_home/workspace/pipelinetest1/mta.jar -help"

// sh "java -jar /opt/sap/mta.jar --build-target=CF --mtar=shine-cf.mtar build"
 
   
}

stage("Deploy")
{
   
 withCredentials([usernamePassword(credentialsId: 'CFDeployShine', passwordVariable: 'CF_PASSWD', usernameVariable: 'CF_USER')]) 
{
       
//sh "/opt/sap/cf deploy shine-cf.mtar --user=$CF_USER --passwd=$CF_PASSWD -s= -o=...."

//todo: 
//herausfinden wo cf liegt
//deploy commando für CF vervollständigen

//Wolfram muss das mtar.jar in Jenkins-Docker reinpacken
//Credentials pflegen bei Jenkins Credentials
//in Jenkinsfile rausziehen


 
       
    }


}

}