# SE-Git-hw

This is my repo for the Git/GitHub homework assignment. It covers creating a repository, branching, pull requests, resolving a merge conflict on purpose, and tracking work with issues.

## Files

- `hello_world.py` - prints `Hello, World!`
- `apple.py` - prints `I eat apple`, added on a separate branch called `feature-1`
- `README.md` - this file

## What I Did

I created the repo, cloned it to my computer, and pushed an initial commit. I made a feature branch, pushed it, opened a pull request to merge it into main, and merged it after it was reviewed.

## The Merge Conflict

I intentionally created a merge conflict to practice resolving one. I changed the same line in `hello_world.py` on two different branches — on `main` I changed it to:

print("Hello, World! This is the main branch version.")


and on a separate branch called `conflict-demo`, I changed the same line to:

print("Hello, World! This is the conflict-demo branch version.")


When I tried to merge them, Git stopped me with:

CONFLICT (content): Merge conflict in hello_world.py
Automatic merge failed; fix conflicts and then commit the result.


I opened the file and found the conflict markers:
<<<<<
print("Hello, World! This is the conflict-demo branch version.")

print("Hello, World! This is the main branch version.")


I picked the version I wanted to keep, deleted the three marker lines, saved the file, then ran:

git add hello_world.py
git commit -m "Resolve merge conflict in hello_world.py"


and that completed the merge.

## Issues & Resolutions

| Issue | Assigned To | Description | Resolution | Status |
|---|---|---|---|---|
| #1 | me | Confirm hello_world.py runs correctly | Ran `python hello_world.py` and confirmed it printed "Hello, World!" as expected | Closed |
| #2 | classmate | Review hello_world.py | Confirmed the script runs correctly | Closed |

## Author

Mudashiru Arowolo
