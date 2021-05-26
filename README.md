# test repository

Used for testing pre-commit hooks and other automations.

## usage with pre-commit

```bash
# install pre-commit
pip3 install pre-commit

# the following commands should be done in the root of this repo

# install this repo's pre-commit hooks
pre-commit install

# see that no files are checked unless they're staged (or in -a/-all mode)
pre-commit run

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
