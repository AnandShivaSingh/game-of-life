pipeline
{
   agent
   {
       node
       {
           label "master"
       }
   }
environment
{
  repo = "https://github.com/AnandShivaSingh/game-of-life"
  MAVEN = tool 'maven'
  jenkins_git_user = "AnandGitHub"
  Major_Version=1
  Minor_Version=1
  Branch = "master"
  


}

stages
    {

stage("Setup")
{
   steps
   {
       script
       {
   PackageVersion = "${env.Major_Version}"+"."+"${env.Minor_Version}"+"."+"${env.BUILD_NUMBER}"
   currentBuild.displayName = PackageVersion
   currentBuild.description = "Branch " + "${env.Branch}" + " Build"
       }
   
			
   
    }
}

stage("checkout Github Repository")
{
   steps
   {
               echo("CHECKOUT REPOSITORY...")
				git credentialsId: "$env.jenkins_git_user", url: "$env.repo", branch: "$env.Branch"
   
   }



}

stage("BUILD")
{
   steps
   {
         echo ("====== START BUILD =======")
     
      script	 
	  {
	  echo "Building started"
	  sh "${env.MAVEN}/bin/mvn -B -V clean package"
	  }
   
   }



}

}


}

