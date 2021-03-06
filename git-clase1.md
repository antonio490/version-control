# Git version control

> Antonio Sanz - Clase 1 "Navigating a commit history"


<kbd> diff -u app.html app_old.html</kbd>



### Using git to view history

I get every commit starting by the most recent. It shows a message and Id to show who made this commit.


<kbd>git log</kbd>

    commit ee54f948c2ef2efece1d7a7d2c59a87d79eb576f (HEAD -> master, origin/master)
    Author: antonio490 <asc490@hotmail.com>
    Date:   Tue Jul 24 20:38:27 2018 +0200

    plotting

    commit 6093a418727136749fd9fcb638dea7d832d5e2a1
    Author: antonio490 <asc490@hotmail.com>
    Date:   Tue Jul 24 20:08:45 2018 +0200

    merge dfs

It can compare two versions of a file.

<kbd>git diff</kbd>

    diff --git a/Numpy and Pandas for 2D Data.ipynb b/Numpy and Pandas for 2D Data.ipynb
    index a622a92..76311df 100644
    --- a/Numpy and Pandas for 2D Data.ipynb        
    +++ b/Numpy and Pandas for 2D Data.ipynb        
    @@ -4162,33 +4162,33 @@
    },
    {
        "cell_type": "code",
    -   "execution_count": null,
    +   "execution_count": 35,
        "metadata": {},
        "outputs": [],
        "source": [
    -    "scaled_entries = data_by_location['ENTRIESn']"
    +    "scaled_entries = data_by_location['ENTRIESn_hourly'] / data_by_location['ENTRIESn_hourly'].mean()"
        ]
    },
    {
        "cell_type": "code",
    -   "execution_count": 32,
    +   "execution_count": 36,



### How often to commit

It is a good idea to keep commits small. As the diff between two versions gets bigger, it gest harder to understand and less useful. A good rule is to make a commit for every logical change. Then each commit will have an specific purpose.

### Multiple files commits

It shows number of insertions, deletions and number of files that have changed on each commit.

<kbd>git log --stat </kbd>

    commit ee54f948c2ef2efece1d7a7d2c59a87d79eb576f (HEAD -> master, origin/master)
    Author: antonio490 <asc490@hotmail.com>
    Date:   Tue Jul 24 20:38:27 2018 +0200

    plotting

     Numpy and Pandas for 2D Data.ipynb | 137 ++++++++++++++++++++++++++++++++++---
    1 file changed, 126 insertions(+), 11 deletions(-)


## Clone a repository

Copy an entire repository on my computer with:

<kbd>git clone url</kbd>

<kbd>git log</kbd>

<kbd>git log --stat</kbd>

### Repository

- Repositories are part of Git. 
- Commits are part of repositories.
- Clone operates on repositories
- Diff operates on Commits
- Log operates on Commits

### Checking prior commits

Checkout older commits

<kbd>git checkout (id) </kbd>


### Configuration Git Workspace

If you already have a file in your home directory named .bash_profile, copy the content from bash_profile_course and paste it at the bottom of .bash_profile. Otherwise, move bash_profile_course to your home directory and rename it to .bash_profile. If you use Linux, you may need to name this file .bashrc instead of .bash_profile.

- git-completion.bash
- git-prompt.sh
- bashrc (Linux)

