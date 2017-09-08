# github_introduction
a brief introduction to GitHub



## To get help

```bash
git help foo
```

_(may be easier to search online to find useful info)_

## To create a new repository:

https://github.com/new

Name the repo and give it a description

For this example the repo is named: `github_intro`

Unless you know for sure you want it to be public, go ahead and make it private (it can be made public later). If you qualify for the education pack (https://education.github.com/pack) you can have unlimited private repos.

When creating a new repo that has no existing content, initialize with a `README` so that it has an initial version and you can just git clone.

If you make a README do the following in the directory where you want the repository cloned:
```bash
git clone github_intro
```

If you have existing code to bring into a project, you will need to `git init`
(git init creates a new repo) in the existing directory and `git add` the files. 

## Making a new repo manually
Create a new directory on your computer, this is where you will be
working from for this particular repo, name it the same as the new repo name.

```bash
mkdir github_intro
cd github_intro

git init 
echo "Something" > README.md
git add README.md
git commit -m "initial commit"

git remote add origin git@github.com:<username>/<RepoName>.git
git push -u origin master
```

## Branching
To begin your repo has one branch to start, this is called master branch.

To create a branch based on master locally (so that you can have a copy on your local machine to work with), you can `git checkout branch <idenitifier and something descriptive about the branch, bug/feature>`.

```bash
git checkout -b username.feature_description
git branch (tells you what branch you are in)
git status (gives you the status of the file)
```

do something to the file, make a change

```bash
echo foobar > foobar
git add foobar
git commit 
git status
git push
```

to see changes:
```bash
git diff master
git status
```

```bash
git push -u origin username.feature_description # push changes and set it as the tracking (upstream) branch
```

on GitHub, open a pull request

## Make and commit changes

Any time you make changes to any existing files or add new files, you must add
those changes to the commit-list, and then commit them before they are part of
the repository.


## standard workflow

- push from branch: `git push origin <branch>`
- create Pull Request on GitHub: through website
- merge on GitHub: through website
- pull on local repo: `git pull origin <branch>`
