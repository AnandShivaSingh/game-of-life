pipeline
{

environment
{
  repo=https://github.com/AnandShivaSingh/game-of-life.github
  jenkins_git_user = "AnandGitHub"
  Major_Version=1
  Minor_Version=1
  Branch = Master
  


}

Stages
    {

stage
{
   steps("Setup")
   {
   PackageVersion = "{$env.Major_Version}"+"."+"${env.Minor_Version}"+"."+"${env.BUILD_NUMBER}"
   currentBuild.DisplayName = PackageVersion
   currentBuild.Discription = "Branch " + "${env.Branch}" + " Build"
   
    }
}

stage
{
   steps("checkout Github Repository")
   {
               echo("CHECKOUT REPOSITORY...")
				git credentialsId: "$env.jenkins_git_user", url: "$env.repo", branch: "$env.Branch"
   
   }



}
}


}

pipeline
{

environment
{
  repo=https://github.com/AnandShivaSingh/game-of-life.github
  jenkins_git_user = "AnandGitHub"
  Major_Version=1
  Minor_Version=1
  Branch = Master
  


}

Stages
    {

stage
{
   steps("Setup")
   {
   PackageVersion = "{$env.Major_Version}"+"."+"${env.Minor_Version}"+"."+"${env.BUILD_NUMBER}"
   currentBuild.DisplayName = PackageVersion
   currentBuild.Discription = "Branch " + "${env.Branch}" + " Build"
   
    }
}

stage
{
   steps("checkout Github Repository")
   {
               echo("CHECKOUT REPOSITORY...")
				git credentialsId: "$env.jenkins_git_user", url: "$env.repo", branch: "$env.Branch"
   
   }



}
}


}

