![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Git

## Introduction

Being able to use both, git and GitHub, is an important skill every software/data engineer must possess. This is even more important when it comes to the ability to handle codes in collaborative projects. This lab will help you learn how to use git/GitHub and understand its importance.

## Instructions

1. First of all, install git if you don't have it yet, and create a GitHub account. ( _You can refer to the lesson "Install Git and Create GitHub Account" in the prework. Follow the guidelines given there. Additionally, you can use these resources: [Install git](https://git-scm.com/downloads), [Version control with git](http://swcarpentry.github.io/git-novice/)_)

Done

2. Create a new repository in the GitHub. Name it `Iron`+ your name. Example: if your name is _Alvaro_, you will name the repo `IronAlvaro`.

https://github.com/MelanieRachel/IronMelanie.git

3. Clone that repo to your computer.

(base) melanie@Melanies-MacBook-Pro Morning % ls
IronMelanie	lab-bash	lab-git

4. Create a file in that folder. Name it `about.txt` and add a fun fact about yourself. (_You can use the command line: `touch nameOfTheFile.txt`_).

(base) melanie@Melanies-MacBook-Pro Morning % ls
IronMelanie	lab-bash	lab-git
(base) melanie@Melanies-MacBook-Pro Morning % cd IronMelanie
(base) melanie@Melanies-MacBook-Pro IronMelanie % touch about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % ls
about.txt

5. Add the file you just created to the git.

(base) melanie@Melanies-MacBook-Pro IronMelanie % git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	about.txt

nothing added to commit but untracked files present (use "git add" to track)
(base) melanie@Melanies-MacBook-Pro IronMelanie % git add about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   about.txt


6. Commit the changes.

(base) melanie@Melanies-MacBook-Pro IronMelanie % ls
about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % echo "Hello" >> about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % ls
about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % cat about.txt
Hello
(base) melanie@Melanies-MacBook-Pro IronMelanie % echo "Sometimes I break out into singtalking"   
Sometimes I break out into singtalking
(base) melanie@Melanies-MacBook-Pro IronMelanie % ls
about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % cat about.txt
Hello
(base) melanie@Melanies-MacBook-Pro IronMelanie % echo "Sometimes I break out into singtalking" >> about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % ls
about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % cat about.txt
Hello
Sometimes I break out into singtalking

7. Push the changes to the GitHub and check your repository to make sure everything is there.

(base) melanie@Melanies-MacBook-Pro IronMelanie % git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   about.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   about.txt

(base) melanie@Melanies-MacBook-Pro IronMelanie % git add about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % git commit -m "Updated info"    
[main (root-commit) efb0541] Updated info
 1 file changed, 2 insertions(+)
 create mode 100644 about.txt
(base) melanie@Melanies-MacBook-Pro IronMelanie % git log
commit efb0541666c7a097e1f5483f5f4683dfa3e2ae2d (HEAD -> main)
Author: MelanieRachel <142107968+MelanieRachel@users.noreply.github.com>
Date:   Sat Sep 9 17:39:48 2023 +0200

    Updated info
(base) melanie@Melanies-MacBook-Pro IronMelanie % git remote -v
origin	https://github.com/MelanieRachel/IronMelanie.git (fetch)
origin	https://github.com/MelanieRachel/IronMelanie.git (push)
(base) melanie@Melanies-MacBook-Pro IronMelanie % git remote -v
origin	https://github.com/MelanieRachel/IronMelanie.git (fetch)
origin	https://github.com/MelanieRachel/IronMelanie.git (push)
(base) melanie@Melanies-MacBook-Pro IronMelanie % git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 279 bytes | 279.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MelanieRachel/IronMelanie.git
 * [new branch]      main -> main

https://github.com/MelanieRachel/IronMelanie/blob/main/about.txt

Great! This was pretty smooth, we hope. :rocket:

Now let's practice the collaboration part.

### Pair Programming Exercise

Pair yourself with a classmate. Send the link of your GitHub repository to your pair via Slack. Now each of you should perform the following set of actions:

1. Fork your classmate's repository. X

https://github.com/Dani-Yana/IronDani.git

2. Clone the repository, so that you have it locally and can make changes. X

(base) melanie@Melanies-MacBook-Pro Morning % ls
IronMelanie			lab-git
lab-bash			lab_solutions.textClipping
(base) melanie@Melanies-MacBook-Pro Morning % git status
fatal: not a git repository (or any of the parent directories): .git
(base) melanie@Melanies-MacBook-Pro Morning % git clone https://github.com/Dani-Yana/IronDani.git
Cloning into 'IronDani'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

3. Create a new branch named `classmate`.

(base) melanie@Melanies-MacBook-Pro Morning % ls
IronDani			lab-git
IronMelanie			lab_solutions.textClipping
lab-bash
(base) melanie@Melanies-MacBook-Pro Morning % cd IronDani
(base) melanie@Melanies-MacBook-Pro IronDani % ls
about.txt
(base) melanie@Melanies-MacBook-Pro IronDani % git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
(base) melanie@Melanies-MacBook-Pro IronDani % git branch classmate
(base) melanie@Melanies-MacBook-Pro IronDani % git branch -a
  classmate
* main
  remotes/origin/HEAD -> origin/main
  remotes/origin/main


4. Create a new file with your name (ex. `maya.txt`) and finish the following sentence _I enrolled Ironhack's Data Analytics bootcamp because..._. When you are done, save the changes. X

(base) melanie@Melanies-MacBook-Pro IronDani % git switch classmate
Switched to branch 'classmate'
(base) melanie@Melanies-MacBook-Pro IronDani % git status
On branch classmate
nothing to commit, working tree clean
(base) melanie@Melanies-MacBook-Pro IronDani % ls
about.txt
(base) melanie@Melanies-MacBook-Pro IronDani % cat about.txt
Fun Fact About Dani: I love turtles.%                                           (base) melanie@Melanies-MacBook-Pro IronDani % touch melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % ls
about.txt	melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % echo "I enrolled Ironhack's Data Analytics bootcamp because I love data" >melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % ls
about.txt	melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % cat melanie.txt
I enrolled Ironhack's Data Analytics bootcamp because I love data

5. Add the changes to the git. X

(base) melanie@Melanies-MacBook-Pro IronDani % git add melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % git status
On branch classmate
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   melanie.txt

6. Commit and push the changes. Now, all the changes should be on your GitHub, inside the forked repository. X 

(base) melanie@Melanies-MacBook-Pro IronDani % git commit -m "Created new file"
[classmate 133a35b] Created new file
 1 file changed, 1 insertion(+)
 create mode 100644 melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % git push origin main
remote: Permission to Dani-Yana/IronDani.git denied to MelanieRachel.
fatal: unable to access 'https://github.com/Dani-Yana/IronDani.git/': The requested URL returned error: 403


7. Create a pull request to make changes appear in the original repository.
8. Merge the branch your classmate created. Now everyone's repos should have the original file (`about.txt`) as well as the new one with your classmate's name.

(base) melanie@Melanies-MacBook-Pro IronDani % git remote -v
origin	https://github.com/Dani-Yana/IronDani.git (fetch)
origin	https://github.com/Dani-Yana/IronDani.git (push)
(base) melanie@Melanies-MacBook-Pro IronDani % cd ..
(base) melanie@Melanies-MacBook-Pro Morning % ls
IronDani			lab-bash			lab_solutions.textClipping
IronMelanie			lab-git
(base) melanie@Melanies-MacBook-Pro Morning % mv IronDani IronDani_old/
(base) melanie@Melanies-MacBook-Pro Morning % git clone https://github.com/MelanieRachel/IronDani.git
Cloning into 'IronDani'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
(base) melanie@Melanies-MacBook-Pro Morning % ls
IronDani			IronMelanie			lab-git
IronDani_old			lab-bash			lab_solutions.textClipping
(base) melanie@Melanies-MacBook-Pro Morning % cd IronDani
(base) melanie@Melanies-MacBook-Pro IronDani % ls
about.txt
(base) melanie@Melanies-MacBook-Pro IronDani % more about.txt 
Fun Fact About Dani: I love turtles.
(base) melanie@Melanies-MacBook-Pro IronDani % ls ../IronDani_old 
about.txt	melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % cp ../IronDani_old/melanie.txt .
(base) melanie@Melanies-MacBook-Pro IronDani % ls
about.txt	melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	melanie.txt

nothing added to commit but untracked files present (use "git add" to track)
(base) melanie@Melanies-MacBook-Pro IronDani % git add melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   melanie.txt

(base) melanie@Melanies-MacBook-Pro IronDani % git commit -m "Lab solved"
[main 6125176] Lab solved
 1 file changed, 1 insertion(+)
 create mode 100644 melanie.txt
(base) melanie@Melanies-MacBook-Pro IronDani % git log
commit 612517621b95b1e879d48ba5d8731ae4258d06d1 (HEAD -> main)
Author: MelanieRachel <142107968+MelanieRachel@users.noreply.github.com>
Date:   Fri Sep 15 17:48:59 2023 +0200

    Lab solved

commit 5499014fa3a6cd601bfb3fb373849c70b69ffaa9 (origin/main, origin/HEAD)
Author: Dani-Yana <daniela.yana1919@gmail.com>
Date:   Tue Sep 12 22:19:32 2023 +0200

    Added about file
(base) melanie@Melanies-MacBook-Pro IronDani % git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 10 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 357 bytes | 357.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MelanieRachel/IronDani.git
   5499014..6125176  main -> main
(base) melanie@Melanies-MacBook-Pro IronDani % 

We hope you enjoyed this activity and learned something new about your classmates! :heart:
