This screencast is about how to contribute to the Akka.net project on GitHub. If you are watching this expecting to learn what Akka.net is all about this is not the screencast for you. What I would suggest is go to http://getakka.net/ website read through the documentation or I can also highly recommend listening to episode 1058 of Dot Net Rocks http://www.dotnetrocks.com/default.aspx?showNum=1058 with guest Roger Alsing. If you are looking for training or looking for a consultant check out http://petabridge.com/.

When I first came across Akka.net I really wanted to contribute. So I decided to create a Dependency Injection extension. But I was so focused on creating the feature I did not take the time to review the best practices prescribed by the Akka.net team. As a result of that misstep I decided to create this screencast to help those whom would like to contribute but have never actually done a Pull Request before. All the steps are outline on the Akka.net GitHub repository and they will be the basis of the screencast.

So the first thing you are going to need is a GitHub account. If you have one then you check off step one complete. If you don't then just go to http://github.com and create an account which is free, quick and easy to do. There are many benefits besides creating pull requests and I would suggest going through their tutorials which are full of excellent information.

Okay next thing on the check list is git the application. In this screencast I will be going through this process from a Windows perspective however everything is still relevant even if you are on Mac or Linux it just means that you path to install the tools will be different. On the Windows side the easiest thing is to install GitHub for windows. The link to the free installation can be found at https://help.github.com/articles/set-up-git/ which has also links to the aforementioned platforms.

Once you have GitHub for Windows installed take the time to configure it by providing with with your credentials, paths to where you would like the cloned repositories to be copied to, the to off git shell you would like to use and any other settings that are pertinent to your situation. I will be using the GitShell not Powershell but you are more then welcome to use what you wish.

Once you have decided on your shell please open it up and type the following `git config --global credential.helper wincred` what this will do is cache your credentials for use by the command line. This will be very helpful unless you enjoy repeatedly typing in your credentials. Check out the reference for more details at https://help.github.com/articles/caching-your-github-password-in-git/.

Git is also integrated into Visual Studio 2012 and above and there is also another cool tool called [SourceTree](http://r.search.yahoo.com/_ylt=A0LEVxrILSNVPHkAiRZXNyoA;_ylu=X3oDMTE3cHExYzVhBGNvbG8DYmYxBHBvcwMxBHZ0aWQDVklQNTA0XzEEc2VjA292LXRvcA--/RV=2/RE=1428397641/RO=10/RU=http%3a%2f%2f0.r.msn.com%2f%3fld%3dd3wBH9FRN4c6yjvNFIqHLvbzVUCUwMsdW93R-AB2CpUJW5V9L9LtEJWFAJMKHlLTZi7kw6mmiNjnXsH-lVaRTjL2xWt9EJTKb_6ASF-MSt8ScfO3rKlT0jAiy9rNuXoSErYEyjDPxGsplqJLiG0VkYyTwDjoemHJaUZSkBz-t-IHVBPcSY%26u%3dhttps%253a%252f%252fwww.atlassian.com%252fsoftware%252fsourcetree%252foverview%253futm_source%253dbing%2526utm_medium%253dcpc%2526utm_term%253dsourcetree%2526utm_campaign%253dSourcetree-US-Brand/RK=0/RS=.dgGgbT6ePIQg87HBJpORR1kgEY-?p=sourcetree). I will be concentrating on using GitHub for Windows along with the GitHub shell but at the end I will go through the other tools.

Great so you have a GitHub Account and you have GitHub for Windows installed and Configured. So the next step is to Fork the Repo. To do that navigate to https://github.com/akkadotnet/akka.net/ then click the Fork Button. This will create essential a clone of the project under your github account. 

Now before we go to far you might want and navigate to https://github.com/akkadotnet/akka.net/blob/dev/CONTRIBUTING.md and take a few minutes to either print this out or keep it open on another screen. This will provide a reference of all the steps we will be taking and was something I personally missed the first time I creates a Pull Request.

So at this point you have an account on github with a forked copy of Akka.net now you need to clone that to your local machine. This can be done either by the using the Git Shell or Git Hub for Windows. Either way it's pretty straight forward. With GitHub for Windows you click the Add new Repository button or just type git clone from the command line (demonstrate both approaches).

Next step is to add the upstream information that we will use to synch of fork version with the Akka.net project code. (demonstrate the process)

Okay now the next thing we are going to have to do is isolate our work by creating a feature branch. This will provide a place to create that new feature or fix a bug to help Akka.net become even more awesome then it already is. (demonstrate creating branch)

At this point we switch to the feature branch and start coding. Go ahead and work through your solution making commits. If your work only takes a short time to complete anywhere from hours to days continue working until you are satisfied with your solution. When you reach that point you need to consider a few things. If you have a bunch of commits that ideally should be one the you should consider squashing those commits into a single commit. (demonstrate squashing). The next thing you are going to want and do is check if the upstream has any new commits. (demonstrate pull from upstream) and merge those changes. After you merge then you want and want to perform a rebase and correct any potential conflicts.

Rebasing will ensure that you pull request is linked once. Show Diagram.

Next step is to navigate back to the Akka.net site and create the Pull Request by clicking Pull Request. Demonstrate Process.

Just like that you have created your first pull request. You can monitor the activity of your request via the site. The core committers may ask you to make some changes but at this point you are all done.

Thanks for watching.