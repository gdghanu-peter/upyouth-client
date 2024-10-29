# UpYouth - Website Project Repo

**Everyone except the repo owner** must push new commits to their respective branch first then create pull request. The repo owner will test the changes to see if they are satisfactory and bug-free before merging into the master branch.

### To switch to another branch:

```bash
git checkout {branch_name}
```

### To merge into master:

```bash
git checkout master
git merge {your_branch}
```

Or create a pull request here. **Absolutely no rebasing into master**.

### To undo back to the most recent commit:

```bash
git reset HEAD~1
```

if you accidentally committed to the wrong branch.

```bash
git reset --hard HEAD (or the branch ID you want to reset to)
```

if you accidentally pushed to the wrong branch (**USE WITH CAUTION**).

### To pull all commits from master into your branch:

```bash
git fetch
git rebase origin/master
```

### To clone the project:

```bash
git clone https://github.com/gdghanu-peter/UpYouth
```

and open the directory with any text editor of your choice.

After cloning, remember to run `yarn install` to download the necessary dependencies. By default, the folder containing dependencies will not be uploaded as it can be quite large.

### To update the latest commits/dependencies:

```bash
git fetch
yarn upgrade
```

It is recommended to do this daily to avoid version conflicts.

### To push a new commit to the repository:

```bash
git push
```

or use the **Source Control** extension in VScode. (It will appear in the menu automatically after installing Git.)

### To host on localhost and start coding:

```bash
yarn dev --open
```

This will host the project's root folder on `localhost:3000` (or another port) and open the default browser.

```bash
yarn dev
```
## Production

Build the application for production:

```bash
yarn build
```

Locally preview production build:

```bash
yarn preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
