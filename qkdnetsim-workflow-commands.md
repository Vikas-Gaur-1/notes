# QKDNetSim Workflow Commands

## 1. Cloning the Repository
```bash
git clone "git@github.com:Vikas-Gaur-1/qkdnetsim-v2.git"
```

## 2. Checking Git Status and Branch
```bash
# View current git status
git status

# Check current branch
git branch
```

## 3. Checking Remote Repositories
```bash
git remote -v
```

## 4. Fetching Updates from Upstream
```bash
git fetch upstream
```

## 5. Switching to Upstream's Branch
```bash
git checkout upstream/main
```

## 6. Resetting Local Branch to Match Upstream
```bash
# Reset local main branch
git reset --hard upstream/main

# View changes to be pushed
git status
```

## 7. Pushing Changes to Fork
```bash
git push origin main --force
```

## 8. Adding Files to Git
```bash
# Add specific untracked file
git add .lock-ns3_linux_build

# Add all files in build directory
git add build/
```

## 9. Committing Changes
```bash
git commit -m "Add .lock-ns3_linux_build and build files"
```

## 10. Setting Tracking Branch (Optional)
```bash
git branch --set-upstream-to=upstream/main main
```

## Summary of Key Commands
1. `git clone`
2. `git status`
3. `git branch`
4. `git remote -v`
5. `git fetch upstream`
6. `git checkout upstream/main`
7. `git reset --hard upstream/main`
8. `git push origin main --force`
9. `git add`
10. `git commit`
11. `git branch --set-upstream-to`

**Note**: These commands facilitate repository management, syncing with upstream, and tracking changes in the qkdnetsim project.
