04-01-2025

CVS and SVN : centralized version control , through which developer used to communicate
and the code is uploaded to one central and then the other can be using it 
If central server went down their would be no way to communicate

GVS : git version control 
Distributed system
Git : it is open source , version control tool 
GitHub : Stores the files in git

it project can be tracked and the version can be rolled back

Git life cycle :

git init : git repository is created. Initation
git add filename/. : files are tracked
git commit : saves the changes
git reset --hard id_of_the_needed_version : rollback to the required version of the file or previous version

#### **Daily lifecycle:**
git add && git commit  && git push


Brach : 
These branches are long-lived and form the core of the project's history. 

- **`main` (or `master`)**: This is the default and primary branch in a repository, representing the official release history and production-ready code. Commits on this branch are often tagged with version numbers.
- **`develop`**: Used in the Gitflow workflow, this branch serves as the integration branch for ongoing development. All completed feature work is merged here before eventually being moved to `main` via a release branch.

#### Supporting branches
- **Feature Branches (`feature/*`)**: Created to develop new features or significant bug fixes. They branch off `develop` (in Gitflow) or `main` (in GitHub flow) and allow developers to work in isolation until the feature is complete and tested.
- **Bugfix Branches (`bugfix/*`)**: Semantically similar to feature branches, these are specifically for fixing non-critical bugs as part of the normal development cycle, typically branching from and merging back into `develop`.
- **Hotfix Branches (`hotfix/*`)**: These are crucial for quickly patching an issue in the live production version (the `main` branch) that requires immediate action. They branch directly from `main` and, once fixed, are merged back into both `main` and `develop` to ensure consistency across the codebase.
- **Release Branches (`release/*`)**: Used to prepare for a new production release. They are branched from `develop` when it's near completion, allowing for final bug fixes, testing, and version bumping in isolation, while development on the next version can continue in `develop`. Once ready, they are merged into both `main` and `develop`.

#### .git folder 
The specific files and directories within a folder may vary slightly depending on the version of Git, but generally include:
- **`HEAD`**: This file is a symbolic reference to the branch you are currently working on (e.g., `ref: refs/heads/main`). It tells Git where to find your current working revision [1, 2].
- **`config`**: This file stores project-specific configuration options, such as remote repository URLs, user information (if overridden from global settings), and branch-specific settings [1].
- **`description`**: This file is only used by the GitWeb program and isn't crucial for most operations [2].
- **`hooks/`**: This directory contains script files that can be run automatically at certain points in the Git lifecycle (e.g., before a commit, after a receive) [1].
- **`info/`**: This directory contains global exclusion patterns in the `exclude` file, which is a per-repo version of `.gitignore` that is not committed to the repository [2].
- **`objects/`**: This is the main storage area for your data. It contains every version of every file, directory, and commit you have ever made, stored as compressed objects [1, 2].
- **`refs/`**: This directory stores references to commits, most notably the locations of local branches and tags (in subdirectories `heads/` and `tags/` respectively) [1].

What the folder does

The folder is responsible for managing your project's version control. It performs several key functions:

- Tracks changes: It monitors all modifications to the files in your project directory [2].
- Manages history: It stores a complete history of all commits, allowing you to view previous states of the project, revert changes, and trace the evolution of your codebase [1].
- Facilitates collaboration: It enables you to interact with remote repositories (like those hosted on GitHub or GitLab), pushing your changes and pulling updates from others [1].
- Enables branching: It allows you to create separate lines of development (branches) without interfering with the main codebase, merging them back in when ready [2]. [[12]
  
#### git branch
-  branch 
- switch : modern version of checkout. It's single purpose is to switch but to restore files use 'restore' command . it is lightweight 
- checkout : older version. Here it switches the branches and restore files and it is overload

#### git merge
- cherry-pick : if there are one or two commits
- merge
- rebase
![[Pasted image 20260105105904.png]]


Learn in depth about merge ,rebase and cherry pick
