# Steps for mirroring to gitHub

## Step 1: Verify we're in the right place and state

```shell
# Check current directory
pwd

# Should show: /Users/sean.middleton/gitea/smiddleto/make-your-game

# Check current branch
git branch

# Should show: * dev

# Check git status
git status

# Should show: working tree clean

```

## Step 2: Verify repository state

```bash
# Optional: Check remote tracking 
git log --oneline -3 origin/dev
git log --oneline -3 origin/main
# Check we have the right remotes
git remote -v

# Check recent commits are there
git log --oneline -2

# Verify main branch exists and is different
git log --oneline -2 main

```

## Step 3: Push to gitea first

```bash
git push origin dev
git push origin main

```

### Important Notes

#### Gitea "fatal" Error Messages

When pushing to Gitea, you may see messages like:
>`remote: fatal: ambiguous argument '...' unknown revision or path not in the working tree.`

**This is harmless** - it's a server-side hook issue, not a git problem. Your push still succeeds if you see:
>`To https://01.gritlab.ax/git/smiddleto/make-your-game.git oldcommit..newcommit  branch -> branch`

## Step 4: Prepare for GitHub

```bash
# Backup current user name
echo "Current user.name: $(git config user.name)"

# Change to GitHub user name
git config user.name "Seán David Middleton - MiddSea"

# Verify change
git config user.name

```

## Step 5: Push to GitHub

```bash
# Check GitHub remote is reachable
git ls-remote github

# Push both branches
git push github dev
git push github main

```

## Step 6: Restore original config

```bash
git config user.name "Seán David Middleton - smiddleto"

# Verify restore
git config user.name
```

---

### Additional Checks

- Verify GitHub authentication works
- Confirm pushes created/updated branches on GitHub
- Check for any merge conflicts or issues

### Additional suggestions:

- Check if GitHub requires authentication
- Verify the pushes actually created/updated branches on GitHub
- Maybe check if there are any conflicts or issues
