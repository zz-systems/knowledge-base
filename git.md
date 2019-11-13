# Remove files that are listed in the .gitignore but still on the repository
[https://stackoverflow.com/a/13541721]
* `git rm --cached file1 file2 dir/file3`
* ``git rm --cached `git ls-files -i --exclude-from=.gitignore` ``
