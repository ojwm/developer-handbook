# Version Control

## Branching strategy

Agree on a branching strategy that fits the team's workflow.

### Feature based development

* [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) - a popular strategy for feature based development.
* [OneFlow](https://www.endoflineblog.com/oneflow-a-git-branching-model-and-workflow) - an evolution of Gitflow to be more efficient and linear.

### Trunk based development

[Trunk-based development](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development) is more suited to DevOps teams using CI/CD.

## Git usage

Using Git is hard and messing up is easy.

Refer to [Oh Shit, Git!?!](https://ohshitgit.com) (or the profanity free version: [Dangit, Git!?!](https://dangitgit.com)).

[Tower](https://www.git-tower.com) offer a free [ebook](https://www.git-tower.com/learn/git/ebook) and also have a comprehensive [FAQ](https://www.git-tower.com/learn/git/faq).

### Renaming branches

1. Checkout the branch and rename it.

   ```sh
   git branch -m new-name
   ```

If the branch has previously been pushed to the remote, it will need renaming there as well.

1. Push to the remote:
   1. `:old-name` deletes the branch with the old name.
   1. `new-name` creates the branch with the new name.

   ```sh
   git push origin :old-name new-name
   ```

1. Set the remote tracking reference for the new branch.

   ```sh
   git push -u origin new-name
   ```

### Squashing commits

#### During merge

```sh
git checkout master
git merge --squash feature/my-feature
```

#### During development

1. Start an interactive rebase on the commit prior to the commit that other commits will be squashed onto.

   ```sh
   git rebase -i HEAD~4
   ```

1. Select the commits to be squashed, by replacing `pick` with `s`.

   ```sh
   pick ca4b127 Working on new feature
   s 2050f54 Some changes
   s 77e50eb Some more changes
   s 1853c79 Fixed stuff
   ```

1. Save the choices (`:x` if using vi).
1. Update the commit message and save to finish the rebase.
1. Force push to the remote, if necessary.

### Commit author and time

Sometimes it's necessary to reset the commit author an time, e.g. when squashing commits on a feature branch before merging to master.

```sh
git commit --amend --reset-author --no-edit
```
