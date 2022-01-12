---
title: Collaboration (Git/Github)
---
# Create a SEA Resource Repo

    As a participant of SEA, I can quickly access (and change) resources which are important for the training.

## Dojo

:include-image: img/dojo_local.png {fit: true}

### Setup

* Set default branch to "main"
* `git config --global init.defaultBranch main`

#### Step 1: Create a local git repository

* `git init`

#### Step 2: Add a new file to the repo (eg. links.md)

* create file links.md
* `git add links.md`

#### Step 3: Commit the new file

* `git commit -m "New file created."`

#### Step 4: Create a new repository on GitHub

* github.com im Browser aufrufen
* eigenes repo unter eigenem User erstellen (zb https://github.com/WildCodeSchool/)

#### Step 5: Set Origin on local Repo

* Copy Repo URL (REPO_URL) from GitHub (HTTPS!)
* `git remote add origin ${REPO_URL}`

#### Step 6: Push the changes to the GitHub Repo

* `git push origin main`

_Note_: GitHub Personal Access Token is necessary here, see file [links.md]

#### Step 7: Clone Repo to new local Repo

* `cd ..`
* `git clone ${REPO_URL} sea-resources-clone`

#### Step 8: Add new links to the links.md

* `git add links.md`
* `git commit -m "Links hinzugefügt."`

#### Step 9: Push the changes

* `git push origin main`

#### Known Issues

##### Q: "main and master are entirely different commit histories."  
##### A: https://stackoverflow.com/questions/23344320/there-isnt-anything-to-compare-nothing-to-compare-branches-are-entirely-diffe

# Merge a SEA Resource Repo

    As a participant of SEA, I want to add new resources to the existing GitHub Repo.

## Dojo

:include-image: img/dojo_git_1.png {fit: true}

### Setup

(Co) Step 1a: Create a local git repository  
(Co) Step 1b: Add a new file with at least one line to the repo  
(Co) Step 1c: Commit the new file  
(Co) Step 1d: Create a new repository on GitHub  
(Co) Step 1e: Push local changes to GitHub

(Mo) Step 2: Clone Repo (...) to local Repo  
(Mo) Step 4: Change first line of newfile.txt and commit

(Ch) Step 3: Clone Repo (...) to new local Repo  
(Ch) Step 5: Change first line of newfile.txt and commit

(Mo) Step 6: Push changes to GitHub

(Ch) Step 7a: Push changes to GitHub  
(Ch) Step 7b: Resolve Merge Conflict  
(Ch) Step 7c: Push changes to GitHub

(RR) Step 8a: Clone repo to local repo  
(RR) Step 8b: Watch changes in file newfile.txt

### Known Issues

Q: After creating a README, I cannot connect my local Repo to the GitHub one (unrelated histories)  
A: "git pull origin main --allow-unrelated-histories"