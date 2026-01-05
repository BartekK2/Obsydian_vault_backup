### Zadania 

#### 1)
There are two files created in the root project directory - A.txt and B.txt.
The goal is to commit only one of them.

```sh
git add A.txt
git commit -m "Commit A.txt file"
```

![[Pasted image 20251104122230.png|400]]

#### 2)
There are two files created in the root project directory - A.txt and B.txt. They are both added to the staging area.
```sh
git reset A.txt
git commit -m "Commit B.txt file"
```

**git reset ściąga z staging area**
#### 3)
It is often good idea to tell Git which files it should track and which it should not. Developers almost always do not want to include generated files, compiled code or libraries into their project history.

Your task is to create and commit configuration that would ignore:

- all files with exe extension
- all files with o extension
- all files with jar extension
- the whole libraries directory
```sh 
echo *.o > .gitignore
echo *.exe >> .gitignore
echo *.jar >> .gitignore
echo libraries/ >> .gitignore
git add .gitignore
git commit -m "Ignore binary files"
```

**plik .gitignore zawiera to co ma byc pomijane w zmianach**
#### 4)
You are currently on chase-branch branch. There is also escaped branch that has two more commits.

	   HEAD
	     |
	chase-branch        escaped
	     |                 |
	     A <----- B <----- C
You want to make chase-branch to point to the same commit as the escaped branch.

                    escaped
                       |
     A <----- B <----- C
                       |
                  chase-branch
                       |
                      HEAD

```sh
git merge escaped
```

**z racji tego że chase-branch jest bezpośrednio przed escaped wystarczy git merge i napewno nie będzie konfliktów**

#### 5)
Merge conflict appears when you change the same part of the same file differently in the two branches you're merging together. Conflicts require developer to solve them by hand.

Your repository looks like this:

	        HEAD
	         |
	    merge-conflict
	         |
	 A <----- B
	 \
	  \----- C
	      	 |
	another-piece-of-work
You want to merge the another-piece-of-work into your current branch. This will cause a merge conflict which you have to resolve. Your repository should look like this:

		                 HEAD
		                  |
		             merge-conflict
		                  |
		 	A <----- B <----- D
		  \               /
		   \----- C <----/
				 |
		another-piece-of-work

```sh
git merge another-piece-of-work
echo 2+3=5 > equation.txt
git add equation.txt
git commit --no-edit
```

**git merge w przypadku wykluczających sie zmian sprawi że w pliku je zawierającym pojawią się dwie wersje z adnotacją i wystarczy wybrać jedną bądź wykasować je i napisać nową rzecz - utworzy sie nowy commit**
#### 6)
You are working hard on a regular issue while your boss comes in and wants you to fix a bug. State of your current working area is a total mess so you don't feel comfortable with making a commit now. However, you need to fix the found bug ASAP.

Git lets you to save your work on a side and continue it later. Find appropriate Git tool and use it to handle the situation appropriately.

Look for a bug to remove in bug.txt.

After you commit the bugfix, get back to your work. Finish it by adding a new line to bug.txt with

Finally, finished it!
Then, commit your work after bugfix.

```sh
git stash

git commit -am "Fix a bug"
git stash pop
echo "Finally, finished it!" >> bug.txt
git commit -am "Finish my work"
```

**git stash można traktować jako schowek zmian popełnionych w working area od ostatniego commita, git stash dodaje zmiany do schowka i pozwala wprowadzić nowy commit a następnie ściągnąć zmiany**

#### 7)

You were working on a regular issue while your boss came in and told you to fix recent bug in an application. Because your work on the issue hasn't been done yet, you decided to go back where you started and do a bug fix there.

Your repository look like this:

        HEAD
         |
	change-branch-history
	         |
	A <----- B
	 \
	  \----- C
	         |
	     hot-bugfix
Now you realized that the bug is really annoying and you don't want to continue your work without the fix you have made. You wish your repository looked like you started after fixing a bug.

	                 HEAD
	                  |
	         change-branch-history
	                  |
	A <----- C <----- B
	         |
	     hot-bugfix
	     
Achieve that.

```sh
git rebase hot-bugfix
```

**rebase zmienia miejsce, od którego zaczyna się gałąź, tak jakby zmiany powstały po nowszych commitach z innej gałęzi**
#### 8)

File ignored.txt is ignored by rule in .gitignore but is tracked because it had been added before the ignoring rule was introduced.

Remove it so changes in ignored.txt file are not tracked anymore.

```sh
git rm ignored.txt
git commit -am "Remove the file that should have been ignored"
```

**git rm ściąga z staging area flaga --cached nie usunie z dysku**
#### 9)
You have committed a File.txt but then you realized the filename should be all lowercase: file.txt. Change the filename.

```sh
git mv File.txt file.txt
git commit -am "Lowercase file.txt"
```

**git mv to ekwiwalent :
mv stary.txt nowy.txt
git rm stary.txt
git add nowy.txt**

#### 10)

You have committed file.txt but you realized you made a typo - you wrote wordl instead of world.

Edit previous commit so no one would realize you haven't checked the file before committing it.

Pay attention to the commit message, too!

```sh
git commit -a --amend
```

**flaga -a to -all czyli automatycznie dodaj wszystkie zmodyfikowane i usunięte pliki do commitu a flaga --amend nadpisuje poprzedni commit**
#### 11)
You should have finished your work a week ago. However, you had some more important things to do so you have committed the work just now.

As a git expert, change the date of the last commit. Don't be modest - make it look like it was committed in 1987!

```sh
git commit --amend --no-edit --date="1987-08-03"
```

#### 12)
While you were working you noticed a typographic error in file.txt - you wrote wordl instead of world.

Unfortunately, you have made another commit on top of the typo so simple git commit --amend is not enough.

Fix the typographic error by amending commit in history. Pay attention to the commit message, too!
```sh
git rebase -i HEAD^^
# mark the first commit with "edit" command
# fix the typo in the file
git add file.txt
git rebase --continue
# fix the typo in the commit message
```

**patrzymy na ostatnie 2 commity i przechodzimy przez nie po kolei zmieniając wszystkie zaznaczone na edit i idziemy dalej z git rebase --continue**

#### 13)
You have created a commit with very important piece of work. You then wanted to fix something in the last commit so you have amended it. However, you have just realized you have accidentally committed the wrong changes and you desperately need the first version of the commit you have just amended.

However, there is no previous version in the history - you have edited the last commit with git commit --amend.

Your goal is to find the first version of the commit in the repository. It must be somewhere...

Once found, force the commit-lost branch to point at it again and verify the solution.

```sh
git reflog
git reset --hard HEAD@{1}
```

**git reflog pokazuje historię zmian pozycji HEAD-a, czyli każdą operację, która przesunęła HEAD (np. commit, merge, rebase, amend, reset itd.).**

**Ustaw HEAD (i bieżącą gałąź) z powrotem na commit, w którym HEAD był jeden krok temu. --hard oznacza, że nadpisze pliki w katalogu roboczym — wszelkie niezapisane zmiany zostaną utracone**
#### 14)
You have committed both first.txt and second.txt as one commit. However, you made a mistake. You intended to commit first.txt in the first commit and the second.txt in the second one.

```sh
git reset HEAD^
git add first.txt
git commit -m "First.txt"
git add second.txt
git commit -m "Second.txt"
```

#### 15)
You were working on an issue and created two commits introducing very small change. You don't want to mess up your project history so you want to make only one commit that contains changes made in the last two.

Execute git log -2 to see last two commits.

```sh
git rebase -i HEAD^^
# squash
```

#### 16)

You have created a simple bash script in script.sh. However, when you check it out on Unix, it does not have required execute permissions so you can't launch it with ./script.sh without performing chmod +x script.sh beforehand.

Fix it by adding an executable bit for script.sh in Git history.

```sh
git update-index --chmod=+x script.sh
```

#### 17)
You are working on an issue for a long time and you noticed you have done too much. You want your work to be committed in two separate commits instead of one.

Unfortunately, your changes involve only one file so it is impossible to git add different files separately.

Commit all new lines that contains "Task 1" phrase in the first commit and the rest of them in the second.

```sh
git add -p file.txt

git commit -m "First part of changes"
git commit -am "The rest of the changed"
```

**git add -p (patch mode) to tryb który pozwala rozdzielić duże zmiany jednego pliku na dwie osobne**

**przy każdej porcji zmian (chunki) dostajemy opcje:
Stage this hunk [y,n,q,a,d,s,e,?]?**
y — dodaj ten hunk do staging area (zostanie uwzględniony w commicie)
n — pomiń ten chunk
s — split — rozdziel chunk na mniejsze części (Git spróbuje podzielić zmianę liniowo)
e — edit — ręcznie edytuj chunk, wybierając dokładnie, które linie mają być dodane
q — zakończ
? — pokazuje pomoc

#### 18)

You have implemented three different features of a program in three different local topic branches.

      HEAD             ---- B - feature-b
       |              /
	pick-your-features - Z <--- A - feature-a
	                      \
	                       ---- C1 <--- C2 - feature-c
You want to have all these features as single commits in pick-your-features branch.

						HEAD
						 |
				  pick-your-features
						 |
    Z <--- A <--- B <--- C

```sh
git cherry-pick feature-a
git cherry-pick feature-b
git cherry-pick feature-c
# rozwiazano merge conflict
git add -A
git cherry-pick --continue
```

**git cherry-pick jest podobny do git rebase ale działa na pojedynczych commitach nie gałęziach**
#### 19)
You were working on an issue-555 topic branch. You noticed a bug, which you fixed in rebase-complex topic branch. Then, you finished issue-555.

However, you need to have bug fixed in your-master branch without any work done on issue-555.

Situation is as follows:
	
	                your-master
	                     |
	A <--- B <--- C <--- D
	        \
	         E <--- F <--- G - issue-555
	          \
	           H <--- I
	                  |
	            rebase-complex
	                  |
	                 HEAD
Only H and I commits should be rebased onto D.

Try to do this with a single git command.

```sh
git rebase issue-555 --onto your-master
```

#### 20)
Instructions
You have committed two changes but you don't like the order in which they appear in the history. Switch them.

To show commits that needs switching, execute git log -2 command.

```sh
git rebase -i HEAD~2
# zamieniamy kolejnosc
```

#### 21)
You noticed that your project contains swearwords. You don't want to remove them in the next commit as your boss might someday find out that they were present in the codebase for a while.

Find all commits that add shit word to either words.txt or list.txt and change them so they introduce word flower instead.

```sh
git log -Sshit
git rebase -i <found commit>^

git rebase --continue
```



