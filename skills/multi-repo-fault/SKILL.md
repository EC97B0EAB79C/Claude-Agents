---
name: multi-repo-fault
description: The auditor steps for the same fault in more than one repository. Fix one repository first, then copy the fix to the others.
---
# Same fault in more than one repository
Log each delegation in the progress file.

## Steps
1. Send one researcher for each repository at the same time. Ask each one if the fault is in its repository, and where.
2. Fix one repository first. Use the repository where the user found the fault.
3. Check the result. If the change is important, get a PASS from the reviewer.
4. Then send one worker for each other repository at the same time. Use the model of the first fix. In **Context**, give the diff command of the first fix.
5. If the project rules say that a file is shared, copy the changed file to the other repositories. Change only the lines that the rules let be different.
6. Commit in each repository on the same branch.
