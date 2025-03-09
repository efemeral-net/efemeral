---
{"publish":true,"title":"⌨️ Git","tags":["shell"],"PassFrontmatter":true}
---


### Initialize

```bash
git init
```

### Check remote

```bash
git remote -v
```

### Set or Change remote

```bash
git remote set-url <name> <newurl>
#such as: git remote set-url origin http://newserver/myproject.git
# git remote set-url main https://github.com/k-hurl-e/job-board-bot.git
```

### Make changes

```bash
git add .
git commit -m "changes being made"
git push
```

### Remove files in .gitignore from repository

```bash
git rm -r --cached .
git add -A
git commit -am 'Removing ignored files'
```

---

## New Repository Connect

```bash
git remote add origin git https://github.com/k-hurl-e/job-board-bot.git
git branch -M main
git push -u origin main
```

```bash
echo "# personalsite" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/keenan-h/personalsite.git
git push -u origin main
```

---

### New Branch

```bash
git branch <branch-you-want>
```

### Switch to branch

```bash
git checkout <branch-you-want>
```

### Commit to new branch

```bash
git commit -m "changes being made"
```

### Push to new branch

```bash
git push -u origin <branch-you-want>
```

### Check your branch or if there are new changes

```bash
git status
```

### Add existing repository to Github

```python
git init
git add .
git commit -m "Add existing project files to Git"
git remote add origin git remote add origin git https://github.com/k-hurl-e/job-board-bot
git branch -M main
git push -u origin main
git push -u -f origin main
```

---

## Safe way to merge a test branch with main

```
git checkout test
git pull
git checkout main
git pull
git merge --no-ff --no-commit test
```

Test `merge` before `commit`, avoid a fast-forward commit by `--no-ff`,

If conflict is encountered, we can run `git status` to check details about the conflicts and try to solve

```
git status

```

Once we solve the conflicts, or if there is no conflict, we `commit` and `push` them

```
git commit -m 'merge test branch'
git push
```

---

### See hidden files

```bash
CMD + SHIFT + .
```

---

### Change Most Recent Git Message

1. Amend the commit message:
```bash
git commit --amend -m "Add initial project setup"
```

2. Force push the changes:
```bash
git push --force
```

---