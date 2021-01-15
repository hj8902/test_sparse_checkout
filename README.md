# test_sparse_checkout
For testing sparse checkout feature of git.

# How to test
### 1. Clone repository

### 2. Set git config for "sparse checkout"

```
git config core.sparsecheckout true
```

### 3. Make checkout list file

```
vi .git/info/sparse-checkout
```

- Add directories and files to have to be included to current repository.
- Then, save.

### 4. Read tree again
```
git read-tree -m -u HEAD
```

- This is to read tree merged(-m) and updated(-u) with HEAD commit version.

### 5. Check repository

# Check points
1. Actually, this is not for check out directories and files that I wanted to bring.
2. This just makes it hide what you do not want.
3. You can check hidden directories and files through below command.
```
git ls-tree -r main
```
