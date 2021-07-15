# Tricks

```bash
# Remove .env file from cached history local
echo '.env' >> .gitignore
git rm -r --cached .env
git add .gitignore
git commit -m 'untracking .env'
git push origin master
```

```bash
# Remove .env file from git history commited
git filter-branch -f --index-filter "git rm -rf --cached --ignore-unmatch .env" HEAD
git push --force
```

