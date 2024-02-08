Data from Augur for the transition project set.  These are grants through the NSF SI2 program made prior to 2014.  We used manual content analysis to find the online URLs for these projects, and in the process identified a set of repositories that are associated with the software built by each of the grants.  Those URLs were provided to Sean Goggins of the Augur project, which is part of the Linux Foundation https://chaoss.community/.  Augur then downloads all the data that can be found about these repositories, including the full code edit history from git, as well as all the actions on GitHub such as creating issues, commenting on issues, code review etc.

The code in this repository shows the queries used against the downloaded Augur dataset to get just the commits, issues and PR events, look at the notebook file for that  The password to access the Augur database is not included in this repo, but the results of the queries are zipped up into oss_data.zip

To re-run the queries one would need the passwords and then can run the queries and code in the notebooks.  The repo works well with repo2docker (to set up a Docker environment with all the need packages etc.

```
git clone <url>
cd transition_augur
python3 -m pip install jupyter-repo2docker
repo2docker .
```
