General commands:
	ls: 
		list contents of a directory 
	
	cd: 
		move to a directory
			cd ~/desktop/demo
	
	mkdir:
		make a directory

	clear:
		clear screen

Git basic commands:

	git init:
		initialise a git repository
	
	git add <filename>:
		add files to staging area
			git add .
			git add a.php
	
	git commit -m "<message>":
		add a new commit to the repository with message
			git commit -m "add a.php to source"
	
	git checkout <branch|id>:
		checkout a commit to work space. Checkout moves HEAD pointer to current commit
			git checkout master
			git checkout ad939ra

	git rm <filename>:
		delete a file 
			git rm a.php

	git mv <old name> <new name>:
		rename a file or a folder
			git mv a.php b.php

Git info commands:

	git status:
		show what has changed in the work space

	git log:
		show all commits making up the current checkout

	git log --graph --oneline --all --decorate:
		show all commits in the repository as a tree

	git branch -vv:
		show local branches as tracked and untracked
	
	git branch -a:
		show all branches both local and remote

Git branch commands:

	git branch <branch>:
		create a new branch from the current checkout
			git branch feature1

	git branch -d <branch>:
		delete a merged branch. Make sure not to stand on a branch to be deleted
			git branch feature1

	git branch -D <branch>:
		delete any branch. Make sure not to stand on a branch to be deleted

	git merge <branch>:
		merge a branch into the current branch. Make sure to stand on branch to merge into
			git merge feature1

Git remote commands:

	git remote add <remote> <url>:
		add a remote to your repository
			git remote add origin https://github.com/lytrung/demo.git

	git push -u <remote> <branch>: 
		push a new tracked branch to remote
			git push -u origin master

	git push <remote> <branch>: 
		push changes on a local tracked branch to remote. This command only works if your local branch is not behind the remote branch
			git push origin f3

	git clone <url> <folder>:
		clone a remote. The new clone contains a tracked master branch
			git clone https://github.com/lytrung/demo.git somestuff

	git fetch <remote>:
		fetch changes from a remote. No changes happen to local branches
			git fetch origin

	git checkout -b <remote/branch>:
		checkout a new remote branch as an untracked branch
			git checkout -b origin/f2

	git checkout --track <remote/branch>:
		checkout a remote branch as a tracked branch
			git checkout --track origin/f3

	git pull <remote>:
		pull and merge commits on a remote tracked branch to your branch. You must stand on the branch to merge into
			git pull origin

Git settings commands:

	git config --global http.proxy <detail>:
		set proxy to git hub
			git config --global http.proxy http://<username>:<password>@proxy.auckland.natcoll.ac.nz:3128

	git config --global user.name "<name>":
		set author name
			git config --global user.name "Joe Bloggs"

	git config --global user.email "<email>":
		set author email
			git config --global user.email "joe.bloggs@gmail.com"