# Site framework

The website uses [al-folio](https://alshedivat.github.io/al-folio/). For their original instructions, see [old_README.md](old_README.md). Here, we maintain a list of (non-obvious) instructions for how to keep the website up to date. 


Details related to Sierra website:
- address: https://sierra-mlopt.github.io/
- git repo: https://github.com/Sierra-mlopt/Sierra-mlopt.github.io

# How to update main page?

Modify the markdown file [_pages/about.md](_pages/about.md).


# How to update team members?

## Overview

In order to add/remove/change the status of the team members: 
- update the metadata in [_data/team.yml](_data/team.yml)
- (change "alumni" to "true" and create a "movedto" field for moving someone to the alumni section).

In order to add a picture for a team member, place it in the repository [assets/img/team](assets/img/team).

## Details

The following step-by-step procedure allows to directly edit the website
0) Create a github account, and get a nice picture of you (if you want to put one on the website).
Make sure the picture has a reasonable size (otherwise, it will take a while to load). Your picture does not need a high resolution here.
1) Fork the repository (so that you have a copy associated with your git account; see, for instance [help here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo))
1) open a terminal
2) clone the repository by typing (replace **\*\*MY_ACCOUNT\*\*** by your git account)
```
git clone git@github.com:**MY_ACCOUNT**/Sierra-mlopt.github.io.git
```
which should create a new folder "Sierra-mlopt.github.io/" in which you can cd
```
cd Sierra-mlopt.github.io
```
and create a new branch
```
git checkout -b my_name
```
3) add your picture to the directory [assets/img/team](assets/img/team) (please name it "yourfirstname_yourfamilyname" with the appropriate extension: .png, .jpg, or .jpeg)
4) update the metadata in [_data/team.yml](_data/team.yml) (please follow the pattern of other entries)
5) save, commit, and push your changes on the git repo
```
git add assets/img/team/
git add _data/team.yml
git commit -m 'team member update: my name'
git push --set-upstream origin my_name
```

You're all set. Now, you can create a pull request (e.g., using the GitHub web interface) to push your updates to the "main" branch.
An owner of the git repository will have to validate this, and then the website will be updated.
