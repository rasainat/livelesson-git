# Git Commands
- `git init`: initialize current folder as a git repo
- `git clone <URL>`: brings the git repo from <URL> to current folder
- `git status`: tells us what we need to know about the repo

- `git add`: adds <FILE> to the staging area
- `git commit`: open a text editor to write the commit message
    - `git commit -m "MESSAGE"`: writes MESSAGE as a commit without a text editor

- `git log`: shows the log (history) of our commits
    - `git log --oneline`: shows the shorter oneline commit

- `git diff`: compare current uncommitted state with last known git state
    - `git diff --staged`: runs git diff between the staging area and last known state
- `git diff HEAD~<NUMBER>`: compares HEAD with commit <NUMBER> ago (relative)
- `git diff <HASH>`: compares HEAD with the commit in <HASH>

- `git restore --source <HASH or HEAD~> <FILE>`: restore file to <HASH or HEAD~>
    - `git checkout <HASH or HEAD~> <FILE>`: restore file to <HASH or HEAD~>
        - `git checkout <HASH or HEAD~>`: if you forget the file, you end up in the detach
        - `git checkout main`: go back to main
        - `git switch main`: go back to main

# Remotes
- `git remote add <NAME> <URL>`: adds the <URL> as a remote with the name <NAME>
    - <NAME> is by convention called `origin`
- `git remote rm <NAME>`: removes the remote called <NAME>
- `git remote -v`: look at all the remotes you have
- `git push <WHERE> <WHAT>`: pushes the <WHAT> branch to <WHERE>
    - `git push origin main`
- `git pull <WHERE> <WHAT>`: pulls the <WHAT> branch in <WHERE> to local computer
