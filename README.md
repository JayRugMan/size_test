# size_test

## Why
The question: If you add a large file and commit, how do you remove it from the repo history

## Tool to assess success
git-sizer
run with ```--verbose```

## Commands to test
```bash
git filter-branch --tree-filter 'rm -f Resources\Video\%font%.ttf' -- --all
git filter-branch --tree-filter 'rm -f Resources\Video\%font%.ttf' -- --all
```

**Try this tool too**
from [github](https://stackoverflow.com/questions/2100907/how-to-remove-delete-a-large-file-from-commit-history-in-the-git-repository)
[BFG Repo-Cleaner](https://rtyley.github.io/bfg-repo-cleaner/)

Run Tool:
```bash
java -jar bfg.jar --strip-blobs-bigger-than 100M my-repo.git
```

Cleanup:
```bash
git gc --prune=now --aggressive
```
