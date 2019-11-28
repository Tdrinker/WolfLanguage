# Git Crash Course

## Workflow:

### Cloning the repo:
* If you do not have the git repository locally, first clone the repo with: 

  `git clone url-of-the-repo`

### New branch and commit:
* To check which branch you are on:

   `git branch`

* By default, you are on branch **master**, do not work/write code in **master**, instead, checkout a new branch:
  
  `git checkout -b your-branch-name`

  The `-b` flag is for checking out a **new** branch, you can always swap back and forth between existing branches by doing:

  `git checkout some-other-branch`

* After you are ready to save and commit your work so far, first check what files you have changed by doing:

  `git status`

  which will list out all of the files you changed, **M** means modified, newly added files will be recognized as untracked files.

    * You can even see the details of what you actually changed by doing `git diff some-file-name`, not specifying filename and just do `git diff` will list all differences

* Add the files one by one: 

  `git add filename-1 filename-2 filename-3`

  Note: If you do not specify filename and just do `git add .` it will simply add all of the changed files listed by `git status`, its always a good habit to do a `git status` again after `git add` to check

* Now commit your changes by doing:

  `git commit -m "some commit messages"`

* Then push your changes:

  `git push --set-upstream origin your-branch-name`


### Grabbing work from other branches:

* To grab changes from another branch:

  `git fetch`

  `git pull origin branch-you-want-to-grab-from`

   Note: Sometimes after the `git pull` a vim editory will show up, simply type `:q!` to exit the vim editor

* Sometimes there might just be bad luck or you are completely lost, this is probably when you want to ditch everything you have worked on:

  `git reset --hard`

  which will force reset your working repository to `HEAD`, this will wipe out all of the changes that you haven't committed.




## Words of Caution:
* It is never a good habit to push directly to **master**, **master** should only be updated by merging other branches into it.
  

