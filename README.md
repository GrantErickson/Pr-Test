# Pr-Test
The goal of this repo is to demonstrate that when creating a PR the builds that run against this PR run in a special merge branch that merges the code from the PR branch and the target branch. It does not run on the PR Branch but another special merge branch. 

Here is the test
1. Main branch has two simple text files
2. The main branch has an action that gets all the code in the branch and then writes the content of the two files in the branch to the action log. This way the actual content of the files can be inspected after the fact.
3. PR Branch is created
4. File #1 is changed in the main branch and not merged to the PR branch.
5. File #2 in the PR branch is changed
6. A PR is created where a build runs.
7. The action log indicates that the files in the branch that is used by the action during the PR process contain both the change in the PR branch as well as the change made in the main branch.
