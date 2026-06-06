

## Assignment 1 Report
Git Branching & Collaboration – MAI201 MLOps
## Student: Jaskaran Singh
GitHub: gilljaskaran
Course: MAI201 MLOps
## Date: June 5, 2026
Repository: https://github.com/gilljaskaran/mlops-git-assignment-JASKARAN-SINGH
- GitHub Network Graph
The network graph below shows all branches created and merged during this assignment:
- feature/add-readme-details branched from develop and merged via PR #1
- feature/add-dockerignore branched from develop and merged via PR #2
- feature/add-code-of-conduct branched from develop and merged via PR #3
- feature/update-readme branched from develop, caused a merge conflict, which was resolved and
merged
## 2. Branch Protection Rules
Branch protection rules were configured for the main branch with the following settings:
- Require a pull request before merging: YES

- Require at least 1 approval: YES
- Dismiss stale pull request approvals when new commits are pushed: YES
- Require linear history: YES
- Allow force pushes: DISABLED
- Allow branch deletion: DISABLED

## 3. Git Log Output
Output of: git log --oneline --graph --all
- 56a1d56 (feature/update-readme) Add student information
| * c036775 (develop) Modify course information section
| * c4a401f (origin/develop) Add course information
## |/
- 8374542 Merge pull request #3 from gilljaskaran/feature/add-code-of-conduct
## |\
| * addbc60 Add contact section to code of conduct
| * 5a8cc99 Add code of conduct
## |/
- 76387fb Merge pull request #2 from gilljaskaran/feature/add-dockerignore
## |\
| * b59e5b2 Add build directories to dockerignore
| * 8e88cb0 Create dockerignore file
## |/
- 6d9d1aa Merge pull request #1 from gilljaskaran/feature/add-readme-details
## |\
| * 3394f88 Add repository structure section
| * 5c84c81 Add Project description and setup instruction
## |/
- 202c9d6 Initial commit
- Reflection on Merge Conflicts
The most challenging part of this assignment was resolving the merge conflict in Part 3. When both the
feature/update-readme branch and the develop branch modified the README.md file, Git could not
automatically decide which changes to keep and flagged the conflict with <<<<<<<, =======, and
>>>>>>> markers.
At first, it was confusing to understand what these markers meant and which section belonged to which
branch. The fix required manually editing the file in a text editor, carefully removing all three conflict
markers, and making sure both the student information section (from feature/update-readme) and the
course information section (from develop) were preserved in the final file.
After resolving the conflict, the file was staged and committed, and the pull request was successfully
completed. This experience taught me the importance of clear communication in teams — if two
developers know in advance which sections of a file they are each editing, merge conflicts can be
avoided entirely.