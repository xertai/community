# Contributing to XertAI

So, you want to build the next generation of machine learning tools within the XertAI community? Yay! 

In order to contribute to the project, there are a few first steps that everybody has to follow. 

- [Code of Conduct](#code-of-conduct)
- [Contributor License Agreements](#contributor-license-agreements)
- [Setting up your Environment to Contribute to XertAI] (#Setting-up-your-Environment-to-Contribute-to-XertAI)
- [Making a Pull Request (PR) Contribution to XertAI] (#Making-a-Pull-Request-(PR)-Contribution-to-XertAI)

## Code of conduct

All members of the XertAI community must abide by the [Code of Conduct](CODE-OF-CONDUCT.md).

## Contributor license agreement

We'd love to accept your contributions! But before we can merge your pull request, you will have to approve the [Computelify CLA](CLA.md).

Once you submit a pull request, you will be prompted to approve the CLA. This is necessary because you own the copyright to your changes, even
after your contribution becomes part of this project. So this agreement simply gives Computelify permission to use and redistribute your
contributions as part of the project.

## Setting up your Environment to Contribute to XertAI

### If you do not have an SSH public key, create one:

```bash
lsdake@beast-05:~$ ssh-keygen -key ed25519
	(...)
```

## Register ssh key to github land
todo

## Create a folder to contain repositories

```bash
lsdake@beast-05:~$ mkdir repos
lsdake@beast-05:~$ cd repos
```

## Clones the repository from your github profile, making a local copy on the machine

```bash
lsdake@beast-05:~$ git clone git@github.com:lsdake/SDAC.git
	(...)
```

## Creates a reference to the source of truth

```bash
lsdake@beast-05:~/repos/SDAC$ git remote add upstream https://github.com/xertai/SDAC.git
```

# Making a Pull Request (PR) Contribution to XertAI

This is how you submit improvements to the code that you've made, after executing ^^^ all that
Some of these commands are "git magic": just roll with it :). They should be done each time you make a contribution!

## Create a branch to make your improvements

```bash
lsdake@beast-05:~/repos/SDAC$ git checkout -b [BRANCHNAME]
```

## Make your improvements to the project!

Make your changes to any file you want to modify

```bash
lsdake@beast-05:~/repos/SDAC$ git commit .
```

## Retrieves a copy of the references from the source of truth

This updates your local references to the upstream

```bash
lsdake@beast-05:~/repos/SDAC$ git fetch upstream
	(...)
```

## Updates the local copy of the repository with the retrieved copy of the references from the source of truth

```bash
lsdake@beast-05:~/repos/SDAC$ git rebase upstream/main
	Successfully rebased and updated refs/heads/main.
```

## This pushes our local copy that's synced with the Source of Truth to our personal fork of the Source of Truth

??With XertAI's workflow, we protect the main branch of the repository so this is always a safe operation from the project's perspective. It may end up damaging your local copy on github, so be careful! ?

```bash
lsdake@beast-05:~/repos/SDAC$ git push -f
	Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
	To github.com:lsdake/SDAC.git
		eae357c..adade0e  main -> main
```
