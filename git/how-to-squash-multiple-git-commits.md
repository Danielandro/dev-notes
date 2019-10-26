# How to squash multiple git commits

Useful for making the git history cleaner and easier to understand. Also for reformatting commits.

1. Invoke git to start an interactive rebase session

`git rebase -i HEAD~[N]`

Here _N_ represents the number of commits you want to join, starting from the most recent one.

You can also use the `commit-hash` of the commit just before the position the rebase starts from.

Example:

```
871adf OK, feature Z is fully implemented   --- newer commit
0c3317 Whoops, not yet...
87871a I'm ready!
643d0e Code cleanup
afb581 Fix this and that
4e9baa Cool implementation
d94e78 Prepare the workbench for feature Z
6394dc Feature Y                               --- older commit
```

To join all commits after `Feature Y` to the most recent:

`git rebase -i 6394dc`

2. Picking & squashing

Your editor will open showing the list of commits to be joined. Below the list, there will be a comment containing the commands to alter the commits.

Use `pick` to flag the commit you want to squash into, then use `squash` to the sqaushee commits!

Save and close!

3. Create new commit

Git will now run our commands. Our editor will reopen as the squash command requires a new message. We'll see the list of messages for each commit that was squashed. We can delete these and supply a new message for the new commit.

Save. And we're done!

Git log will now reflect the change.

## Resources

- [EggHead.io - Kent C. Dodds](https://egghead.io/lessons/javascript-how-to-squash-multiple-git-commits)

- [Internal Pointers article](https://www.internalpointers.com/post/squash-commits-into-one-git)

---

[Main Page](../README.md)
