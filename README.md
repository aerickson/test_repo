# test repository

Used for testing pre-commit hooks and other automations.

## usage with pre-commit

```bash
# install pre-commit
pip3 install pre-commit

# the following commands should be done in the root of this repo

# install this repo's pre-commit hooks
pre-commit install

# run on all files with verbose
pre-commit run --all --verbose
# It should complain about bad urls in bad.txt.
# - Commit was possible with 'git commit -n' to skip pre-commit hooks.

# testing commit blocking on failure:
# 1. change a file (add a bad URL to see a failure)
vi test_file
# 2. stage the changed file
git add test_file
# 3. try to commit the file. it should fail if a bad URL was added.
git commit -m 'test'
# 4. try committing anyways by bypassing the hooks
git commit -m 'test' -n
```
