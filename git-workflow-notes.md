# Git Workflow for Managing Forked and Upstream Repositories

## Remote Repositories
1. **Forked Repository** (`origin`): Your personal copy of the original repository on GitHub.
2. **Original Repository** (`upstream`): The original repository from which you forked.

## Branch Tracking
* Forked (`origin`) and upstream repositories can have the same branch name (`main`), but they are separate entities.
* When cloning your fork, the default local branch (`main`) will track `origin/main`.
* The `upstream` repository may have a `main` branch, but your local `main` initially tracks `origin/main`.

## Fetching Updates from `upstream`

### Add Upstream Remote
```bash
git remote add upstream git@github.com:QKDNetSim/qkdnetsim-v2.git
```

### Fetch Updates
```bash
git fetch upstream
```

### View Branches
```bash
git branch -a
```

## Working with `upstream/main`

### Create Local Branch Tracking `upstream/main`
```bash
git checkout -b upstream-main upstream/main
```

### Switch Back to Fork's `main`
```bash
git checkout main
```

## Syncing Your Fork with `upstream`

### Reset Local Branch to Match `upstream/main`
```bash
git reset --hard upstream/main
```

### Push Reset Changes to Fork
```bash
git push origin main --force
```

## Setting Tracking Branch
```bash
git branch --set-upstream-to=upstream/main main
```

## Key Points
* `origin` refers to your forked repository
* `upstream` refers to the original repository
* Local `main` branch by default tracks `origin/main`
* Use `git fetch upstream` to fetch updates
* Create separate local branch to track `upstream/main`
* Synchronize fork with original repository by resetting and force-pushing

**This workflow ensures your fork remains up-to-date with the original repository while maintaining control over your changes.**
