# First Contributions

*Read this in other languages: [English](README.md), [Spanish](README.es.md)*

If you don't have git on your machine, [ install it ]( https://help.github.com/articles/set-up-git/ )

<img align="right" width="300" src="assets/fork.png" alt="fork this repository" />  

## Fork this repository

Fork this repo by clicking on the fork button

## Clone the repository

Now clone this repo to your machine. Click on the clone button and then the copy to clipboard icon

<img align="right" width="300" src="assets/clone.png" alt="clone this repository" />  

<img align="right" width="300" src="assets/copy-to-clipboard.png" alt="copy URL to clipboard" />

Open a terminal and run the following git command:

```
git clone "url you just copied"
```
Where "url you just copied" (without the quote marks) is the url to this repository. See the previous steps to obtain the url.

For example:
```
git clone https://github.com/this-is-you/first-contributions.git
```
Where 'this-is-you' is your github username. Here you're copying the contents of first-contributions repository in github to your computer

## Create a branch

Change to the repository directory on your computer if you are not already there.

```
cd first-contributions
```
Now create a branch using `git checkout command`
```
git checkout -b <add-your-name>
```

For example:
```
git checkout -b add-alonzo-church
```

## Make necessary changes and commit those changes

Now open `Contributors.md` file in a text editor and add your name to it, then save the file. If you go to the project directory and do `git status`, you'll see there are changes. Add those changes using `git add`
```
git add Contributors.md
```

Now commit those changes using `git commit`
```
git commit -m "Add <your-name> to Contributors list"
```
replace `<your-name>` with your name

## Push changes to github

Push your changes using `git push`
```
git push origin <add-your-name>
```
Replace `<add-your-name>` with the name of the branch you created earlier

## Submit your changes for review

If you go to your repository on github, you'll see a button to open a pull request. click on that button.

<img style="float: right;" src="assets/compare-and-pull.png" alt="create a pull request" />

Now submit the pull request.

<img style="float: right;" src="assets/submit-pull.png" alt="submit pull request" />

## Keeping your fork synced with this repository

Now I'll be merging all your changes into the master branch of this project. Your fork won't have those changes. In order to keep your fork synced with mine, add my repo's url as `upstream remote url`.
```
git remote add upstream https://github.com/Roshanjossey/first-contributions
```
This is a way of telling git that another version of this project exists in the specified url and we're calling it master. Once the changes are merged, fetch the new version of my repository.
```
git fetch upstream
```

Here we're fetching all the changes in my fork (upstream remote). Now, you need to merge the new revision of my repository into your master branch.
```
git rebase upstream/master
```
Here you're applying all the changes you fetched to master branch. If you push master branch now, your fork will also have the changes
```
git push origin master
```
Notice here you're pushing to the remote named origin.
