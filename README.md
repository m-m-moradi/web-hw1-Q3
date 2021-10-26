## Part 1
```bash
$ git commit --amend -m "amend FileA.txt"
```

## Part 2
```bash
$ echo '.env' >> .gitignore
$ git rm -r --cached .env
$ git add .gitignore
$ git commit -m 'untracking .env'
$ git filter-branch --index-filter "git rm -rf --cached --ignore-unmatch .env" HEAD
$ git push --force
```
