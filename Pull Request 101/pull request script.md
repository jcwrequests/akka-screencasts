# Pull Request - Outline #

##  [Based on https://github.com/akkadotnet/akka.net/blob/dev/CONTRIBUTING.md](https://github.com/akkadotnet/akka.net/blob/dev/CONTRIBUTING.md "https://github.com/akkadotnet/akka.net/blob/dev/CONTRIBUTING.md") ##

1. Create a GitHub Account - https://github.com/
2. Go to Akka.net site https://github.com/akkadotnet/akka.net
3. Fork the project
4. Clone Forked locally
5. Add an upstream remote
	1. git remote add upstream https://github.com/akkadotnet/akka.net
6. Create feature branch locally on the dev branch
	1. Name should be descriptive
7. Work on your new feature committing to the new feature branch
8. As you work through the feature periodically
	1. git checkout dev
	2. git fetch upstream
	3. git merge --ff-only upstream/dev
9. Rebase often
10. Push to changes to forked repo
11. Place holder - need details to submit PR