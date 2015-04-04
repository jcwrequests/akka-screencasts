# Pull Request - Outline #

##  [Based on https://github.com/akkadotnet/akka.net/blob/dev/CONTRIBUTING.md](https://github.com/akkadotnet/akka.net/blob/dev/CONTRIBUTING.md "https://github.com/akkadotnet/akka.net/blob/dev/CONTRIBUTING.md") ##

1. Create a GitHub Account - https://github.com/
2. Install GitHub for Windows which will install the command line tool and GUI
	1. https://help.github.com/articles/set-up-git/
	2. TIP:  https://help.github.com/articles/set-up-git/
		1. git config --global credential.helper wincred
3. Go to Akka.net site https://github.com/akkadotnet/akka.net
4. Fork the project
5. Clone Forked locally
6. Add an upstream remote
	1. git remote add upstream https://github.com/akkadotnet/akka.net
7. Create feature branch locally on the dev branch
	1. Name should be descriptive
8. Work on your new feature committing to the new feature branch
9. As you work through the feature periodically
	1. git checkout dev
	2. git fetch upstream
	3. git merge --ff-only upstream/dev
10. Rebase often
11. Push to changes to forked repo
12. Place holder - need details to submit PR